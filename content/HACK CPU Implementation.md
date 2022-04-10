Status:
Tags:
Links: [[HACK CPU]] - [[Nand2Tetris Project 5]]
___
# HACK CPU Implementation
## Notes
- Took a lot longer than I expected
- I managed to formulate most of the CPU independently, but had troubles with the control inputs for the registers and mux chips
	- I think the main issue that prevented my code from running was the way I calculated the `writeM` output, as I used an `Or Gate` instead of an `And Gate`
	- It was nice to spend some quality time trying to troubleshoot without the assistane of a compiler :p
## Code
```
CHIP CPU {

    IN  inM[16],         // M value input  (M = contents of RAM[A])
        instruction[16], // Instruction for execution
        reset;           // Signals whether to re-start the current
                         // program (reset==1) or continue executing
                         // the current program (reset==0).

    OUT outM[16],        // M value output
        writeM,          // Write to M? 
        addressM[15],    // Address in data memory (of M)
        pc[15];          // address of next instruction

    PARTS:
	//Decoding instruction bit
	
	And(a=instruction[15], b=instruction[15], out=cInstruction);
	Not(in=cInstruction, out=aInstruction);
	
	//Configuring Register and Mux Loads
	
	Or(a=aInstruction, b=instruction[5], out=aLoad); //loads if a instruction or a destination
	And(a=cInstruction, b=instruction[4], out=dLoad); //loads if d instruction or d destination
	And(a=cInstruction, b=instruction[12], out=AorM); //only puts instruction if c instruction or using a register
	
	//Main components
	
    Mux16(a=aluOut, b=instruction, sel=aInstruction, out=instructionOut); //sel = alu out or instruction to A Register
	ARegister(in=instructionOut, load=aLoad, out=regAOut, out[0..14]=addressM); //sel = d1 = store A or no
	Mux16(a=regAOut, b=inM, sel=AorM, out=AorMOut); //sel = a = outputting A or M
	DRegister(in=aluOut, load=dLoad, out=regDOut); //load = d2 = store D or no
	ALU(x=regDOut, y=AorMOut, zx=instruction[11], nx=instruction[10],
		zy=instruction[9], ny=instruction[8], f=instruction[7], no=instruction[6],
		out=outM, out=aluOut, zr=zrOut, ng=ngOut); //zx -> no = c1 -> c6 
	
	//Checking for PC jump
	
	Or(a=zrOut, b=ngOut, out=zrOrNeg); //checks whether number is positive
	Not(in=zrOrNeg, out=pos); //creates pos flag
	Not(in=zrOut, out=notZr);
	
	And(a=instruction[2], b=ngOut, out=jlt); //jump check for negative condition
	
	And(a=instruction[1], b=zrOut, out=jeq); //jump check for zero condition
	
	And(a=instruction[0], b=pos, out=jgtTemp); //jump check for pos condition
	And(a=jgtTemp, b=notZr, out=jgt);
	
	Or(a=jlt, b=jeq, out=jumpTemp);
	Or(a=jumpTemp, b=jgt, out=jumpToA); //checks to see if a jump is valid for any
	And(a=cInstruction, b=jumpToA, out=loadPC); //only jumps if c instruction
	PC(in=regAOut, load=loadPC, inc=true, reset=reset, out[0..14]=pc);
	
	And(a=instruction[3], b=cInstruction, out=writeM); //sets d3 (storage of M) as writeM
}
```
## Truth Table
| time | inM   | instruction      | reset | outM    | writeM | addre | pc  | DRegister |
| ---- | ----- | ---------------- | ----- | ------- | ------ | ----- | --- | --------- |
| 0+   | 0     | 0011000000111001 | 0     | ******* | 0      | 0     | 0   | 0         |
| 1    | 0     | 0011000000111001 | 0     | ******* | 0      | 12345 | 1   | 0         |
| 1+   | 0     | 1110110000010000 | 0     | ******* | 0      | 12345 | 1   | 12345     |
| 2    | 0     | 1110110000010000 | 0     | ******* | 0      | 12345 | 2   | 12345     |
| 2+   | 0     | 0101101110100000 | 0     | ******* | 0      | 12345 | 2   | 12345     |
| 3    | 0     | 0101101110100000 | 0     | ******* | 0      | 23456 | 3   | 12345     |
| 3+   | 0     | 1110000111110000 | 0     | ******* | 0      | 23456 | 3   | 11111     |
| 4    | 0     | 1110000111110000 | 0     | ******* | 0      | 11111 | 4   | 11111     |
| 4+   | 0     | 0000001111101011 | 0     | ******* | 0      | 11111 | 4   | 11111     |
| 5    | 0     | 0000001111101011 | 0     | ******* | 0      | 1003  | 5   | 11111     |
| 5+   | 0     | 1110001100001000 | 0     | 11111   | 1      | 1003  | 5   | 11111     |
| 6    | 0     | 1110001100001000 | 0     | 11111   | 1      | 1003  | 6   | 11111     |
| 6+   | 0     | 0000001111101100 | 0     | ******* | 0      | 1003  | 6   | 11111     |
| 7    | 0     | 0000001111101100 | 0     | ******* | 0      | 1004  | 7   | 11111     |
| 7+   | 0     | 1110001110011000 | 0     | 11110   | 1      | 1004  | 7   | 11110     |
| 8    | 0     | 1110001110011000 | 0     | 11109   | 1      | 1004  | 8   | 11110     |
| 8+   | 0     | 0000001111101000 | 0     | ******* | 0      | 1004  | 8   | 11110     |
| 9    | 0     | 0000001111101000 | 0     | ******* | 0      | 1000  | 9   | 11110     |
| 9+   | 11111 | 1111010011110000 | 0     | ******* | 0      | 1000  | 9   | -1        |
| 10   | 11111 | 1111010011110000 | 0     | ******* | 0      | 32767 | 10  | -1        |
| 10+  | 11111 | 0000000000001110 | 0     | ******* | 0      | 32767 | 10  | -1        |
___
References: