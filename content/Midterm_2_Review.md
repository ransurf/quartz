# Program Control
## Function Call and Stack
- a *caller* calls another function, the *callee*

### Memory Layout
![[Pasted image 20220316202945.png|300]]
- notice there are 64 bits of actual memory addresses, but only 48 of them are actually accessible (m = 64)
- Separate across different section  (KSSHDT)
	- **Kernal** -> system level stuff 
	- **Stack** -> runtime stack for local variables, locally called arrays
	- **Shared Libraries** -> executable machine instructions like printf
	- **Heap** -> Dynamically allocated with malloc, free, new, delete
	- **Data** -> Static variables for globals, constants
	- **Text** -> use for the file to run, initialized by executable
	
### Passing Control
 - **%rsp**
	- stack specific register
	- points at last used byte on the stack
	- initialized at the top of the stack, grows downwards
- **push**
	- push Imm, register, or memory address
	- when pushing
		1. get ***value*** of `src`
		2. decrement %rsp by 8
		3. store value in %rsp
	- %rsp is an *implicit* register in push
- **pop**
	- pop onto a given register
	- when popping
		1. read value of memory address stored in %rsp
		2. store it in dest
		3. increment %rsp by 8
	- %rsp is an implicit register 
- **call**
	- calls a function
	- when calling
		1. push  of PC (program counter -> %rip) onto the stack, this is the return address `pushq %rip`
		2. set PC to first address of func `movq "func", %rip (not actual)`
		3. start executing `jmp func`
	- the "stack frame" begins after the return address of the caller is pushed
- **ret**
	- when returning
		1. pop the return address off the stack and into PC
		2. start executing from that address

### Passing Data - L18
#### x86 Calling Convention 
- *caller*:  move the callee's arguments into the correct registers before calling
	- in order of arguments: rdi, rsi, rdx, rcx, r8, r9
- *callee*: move the returned value to rax
- if there are more than 6 arguments, caller must place the arguments on the stack in reverse order
	- the callee then has to pop these values off the stack in  order
		- note: the displacement will be off because of the addition of the return address on the stack when the function is called 
- if a memory address to a value (a pointer) need to be passed in the function, the value must also be added to the stack first, then the address can be passed with `leaq`

### Managing Local Data - L19
![[Pasted image 20220316212906.png|600]]
#### Callee Saved Registers
- the callee function must preserve the value before using them, and return them to their original values before `ret`
- callee must push these registers onto the stack and pop it to the same register before return 
- *this is the responsibility of callee*

#### Caller Saved Registers
- the caller function must save these values on the stack before calling a function
- includes the argument registers 
- it's the caller's responsability to save these, if they get messed up its not its fault

#### Spilling
- can set up temporary space with %rsp and assign variables 
- allocate space with `subq $16, %rsp`
- assign values with `movq %rax, 8(%rsp)`
- restore stack with `addq $16, %rsp`

### Recursion - L20
- same as regular recursion, each function call has its own stack frame, return addresses, and parameters 
- still have to follow register and function call conventions 

## Arrays
- they're also just pointers 
- these operations give you the same memory address: `x + 1`, `&x[1]`
- these operations give you the same value: `x[4]`, `*(x+4)`   
- in assembly they're just contiguous points in memory 
- calculated with `A[i] = A + i * L`
	- `A` is the address of the first point
	- `i` is the index of the array
	- `L` is the size of the individual element
- allows for quick indexing with memory address indexing via `movq (%array start, index, char size), %register you want to save to`
- allocate by moving %rsp down the stack

### 2D Arrays - L21
- in C an array is just a longer contiguous row of bytes
- accessed with `A[R][C]`, row column, think of it as a the array being stripped into stacks of memory, going downward
	- access each row with `A + (R * C * L)`, where R is the row you want, C is the number of columns, and L is the size
		- jump rows by incrementing by that multiplication 
	- access each column with `A + (C * L)` where C is the column you want 
	- putting it all together, it's `A  + (i * C + j) * L`

# Buffer Overflow - L22
- local variables, calle and caller saved registers, and return addresses are all stored on the stack 
- if a function does this too much it may buffer overflow and overwrite local variables, registers, and return addresses
	- leads to seg faults and system vulnerabilities 
	- called **stack smashing**
- can be prevented with code like (well the idea anway)
```c
if input size <= array size
	write into array
```

## Code Injection 
- attacker overflows the buffer with a string that contains malicious code 
- overwrites the retrun address of the function, and makes it point to more malicious code in the string
- when return it called, %rsp jumps to malicious code and starts running it 

## Defenses
### Avoid Overflow
- design and use functions that check string lengths before writing 
	- safe: `fgets()`
	- unsafe: `gets(), strcpy(), strcat(), sprinf()`
- `strcpy(dest, source)` copies an entire string into memory, including null character (bad)
- `strncpy(dest, source, sizeof(dest))` copies enough characters to fit into the destination, padding with null bytes or truncating the version without a null character (okay)
- `strlcpy(dest, source, sizeof(dest))` copies enough for string and the null character, resulting in one less character than `strncpy()` (good)

### System-Level Protection
- randomize stack offsets
	- system allocates random amoutns of space before main, shifting the address of %rsp 
	- makes it harder for hackers to know where the stack frame starts, and thus where to jump to get to malicious code 
- non-executed code segments
	- in the past, x86 had read-only and writeable permissions, only readable permissions could be executed
	- x86-64 has *executable* permissions, and stack memory is non-executable
- canary values
	- put a randomized canary value between the array and return address
	- check if the canary value has been changed before returning, reporting a failure if it has
- Control-Flow Enforment Technology
	- `endbr64` placed at the front of functions
	- microprocessor checks if indirect call goes to functions that start with `endbr64`, if they don't have the seal of approval the program aborts

# Floating Point Data - L23
- in the 90s processing was sped up with the advent of SIMD -> single instructions on multiple data, and this evolved into two current forms
	- SSE -> Streaming SIMD Extension
	- AVX -> Advanced Vector Extensions 


## XMM Registers
- these registers hold floats and doubles, as opposed to our previous registers which were known as *integer registers*
- 16 bytes wide
- 16 of them, labelled `%xmm0` to `%xmm15`
- has two modes of storage
	- *scalar mode* -> similar to regular registers, each register holds one data
	- *vector mode* -> groups multiple data of smaller type into a single register 

| Data Type       | Count |
| --------------- | ----- |
| Single byte int | 16    |
| 16-bit int      | 8     |
| 32-bit int      | 4     |
| float           | 4     |
| double          | 2     |

### Operations
 - using operands on vector (packed) registers does the operation to each of the items in that register 
 - operands are formated `operand{p/s}{data}` so `addpd` is add packed double, `addsd` is add scalar double, `addss` adds scalar single percision (float)  
- standard memory addressing modes and 
- the `mov` command can have the `ap` flag after it like `movap` which moved the contents aligned and packed to the next register 
	  
### Function Call and Register Saving
- floating point values are saved to the `%xmm*` registers
	- note pointers are still 64 bit, so a pointer to a float still uses the regular registers
- arguments are pasesd in order from `%xmm` 0 to 7
- 8 to 15 are just used for managing local data 
- return value in `%xmm0`
- all registers are caller-saved  

### Data Conversion
- y axis is source, x axis is destination 

	|        | float     | int       | double   | long       |
	| ------ | --------- | --------- | -------- | ---------- |
	| float  |           | cvttss2si | cvtss2sd | cvttss2siq |
	| int    | cvtsi2ss  |           | cvtsi2sd |            |
	| double | cvttsd2ss | cvttsd2si |          | cvttsd2siq |
	| long   | cvtsi2ssq |           | cvtsi2sdq         |            |

### Data Manipulation
![[Pasted image 20220317104028.png]]
# Instruction Set Architecture - L23 
## How Computers Work
- the microprocessor datapath is the way it loads and executes commands
	- ALU (Arithmetic Logical Unit) -> performs calculations
	- Registers -> store data for calcualtions
	- Buses -> allow data to move betwen
- the instruction memory of the cpu holds the machine code for what to do, each time it fetches an instruction is also increments the PC by one to get the next instruction 

## Back to ISA
- defines the memory model and instruction set of the cpu (implements)

### Memory and Registers
- determines the size of a word (how much memory is fetched/written each cycle)
- determines how big the registers are (related to word count) and how many there are
- determines the memory size 
	- calculated with $2^m * n$
	- $2^m$ addressable locations in memory, where m is the number of bits given for memory addresses
	- n is the resolution (size) of each addressable location in memory 
- Example: 
	- x86 has a word size of 64 bits, $2^{64}$ addressable memory locations, and 8 bits for each addressible location in memory (byte-addressable) 
	- it has 16 integer registers and 16 floating point registers

### Instruction Set
- the format, syntax, operands, memory addressing modes
- in both assembly and machine code 
- Example:
	- x86 has lots of instructions, a two/one operand model, and various memory addressing modes 

### Conventions

ISA is a formal specification of
?
- how control and data is passed in function calls
- how registers are preserved during function calls
	- which registered are callee or caller saved?

Example of x86 formal specifications
?
- Example: x86 has registered reserved for callee saved, return addresses, stack pointers, etc. 

### Model of Computation
- when it converts C to machine code the programmer should understand how it happened
- should produce an expected result 

## ISA Guidelines
### 1. Unambiguous Encoding
- the processor can easily decode and execute instructions 
- in assembly, each instruction has specific naming schemes that translate directly into machine instructions 
- this is done with the opcode and operand format 

### 2. Functionally Complete
- turning complete, must have 
	- Data Transfer -> memory reference and storage
	- Data Manipulation -> arithmetic and logical operations
	- Program Control -> branching and jumps 

### 3. Brief
- have as few as possible to simplify your hardware
- must have same length and same format 
	- if the format is different, the fields (sections) of your binary code must be formatted so the fields with the same purpose are at the same location 

## Types of Instruction Sets
### CISC
- Complex Instruction Set Computing
- lots of instructions 
- usually "register-memory" -> any instruction can access memory
- Ex: x86, VAX, MC68000

### RISC
- Reduced Instruction Set Computing
- small general purpose instructions for simpler microprocessor design
- usually "load-store" -> can only access memory with load and store commands
- Ex: **MIPS**, SPARC, Alpha, AXP, PowerPC

# MIPS - L24
Microprocessor without Interlocked Pipelined Stages 

## Memory Model 
- 32 registers
![[Pasted image 20220317120804.png|600]]
- 32 bit word size (hence register is also 32 bits)
- Byte-addressable -> address resolution is 8 bits
- memory size is $2^{32} * 8$, so those many distinct chunks 
![[Pasted image 20220317120836.png|400]]

## Instruction Set
- 3 operand assembly language `add a,b,c` is $a = b + c$
- keeps design simple as variable number of operarnds is complicated
![[Pasted image 20220317121052.png]]
- MIPS machine instructions are fixed length of 32 bits
	- opcode (6 bits)-> operand
	- rs(5) -> first register operand
	- rt(5) -> second register operand
	- rd(5) -> desination register
	- shamt(5) -> shift amount
	- fun(6) -> function code, indicates variant of the opcode
		
![[Pasted image 20220317121255.png]]
- this method does have problems as the contants can only be defined with 5 bits, which is not enough 
- created three differemt formats of instructions, *indicated by the opcode*
	- this format follows the 3rd ISA guideline as different formats still have fields with the same purpose in the same location for each format	

![[Pasted image 20220317121940.png]]