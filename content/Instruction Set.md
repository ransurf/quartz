---
aliases:
---
Status:
Tags: #cards/cmpt295/isa
Links: [[Instruction Set Architecture (ISA)]]
___

# Instruction Set

## Principles
?
- All commands understood by agiven computer architecture
- [[Microprocessor]] implements an ISA
<!--SR:!2022-03-22,1,130-->

### Guidelines

#### Unambiguous Encoding
?
- the processor can easily decode and execute instructions
- in assembly, each instruction has specific naming schemes that translate directly into machine instructions
- this is done with the opcode and operand format

#### Functionality complete
Turing complete must have
?
- Data transfer instructions (memory reference)
- Data manipulation instructions (arith, logical)
- Program control instructions (branch, jump)
<!--SR:!2022-03-22,1,130-->

#### Brief machine instruction format
?
- Few as possible
- Have all same length and format
	- Position fields that have same purpose in same location in format
	- src is always second
- if the format is different, the fields (sections) of your binary code must be formatted so the fields with the same purpose are at the same location
<!--SR:!2022-03-22,1,130-->

### Types
Assembly Instruction
?
- Symbolic representation of machine instruction
	- *ex) movq*
- Labels to represent adresses
<!--SR:!2022-03-22,1,130-->

Machine Instruction
?
- Each assembly instruction has corresponding machine instruction
- Represented as binary

CISC
?
- Complex instruction set computing
- Large # of instructions including special purpose
- usually register-memory architecture
- *ex) VAX, x86, MC68000`

RISC
?
- Reduced instruction set computing
- Small # of general purpose instructions
	- Smaller machine instruction set
	- Simpler microprocessor design
- Load/store architecture
	- Only load/store can access memory
<!--SR:!2022-03-22,1,130-->

### Components
Opcode
?
- Operation that can be executed by microprocessor

Operands
?
- Required by opcode for microprocessor to carry out instruction
- Expressed as binary
<!--SR:!2022-03-22,1,130-->

> **opcode** | operands
___
References:

Created:: 2022-03-14 03:55