---
title: Nand2Tetris Fill Program
---
Status:
Tags:
Links: [Nand2Tetris Project 4](out/nand2tetris-project-4.md)
___
# Nand2Tetris Fill Program
## Objective
- Fills screen to black when a key is pressed
## Tasks
- Infinite loops for when key is pressed, and changing the state of the screen based on that input
	- Listen to keyboard
		- If keyboard input != 0, black 
			- else false
	- Pointers for screen
		- Remember to manually test with **no animation**
## Psuedo-Code
```
if (KBD!=0) {
	for (int reg=SCREEN; SCREEN<SCREEN_END; screen++) {
		reg=-1;
	}
}
```
## Code
```
(RESET)
	@i //amount added to SCREEN value to change
	M=0 //sets i to 0
	@8192  // number of pixels on a screen divided by 16-bit address (256 x 512 / 16)
	D=A    // D = total number of pixels
	@sum 
	M=D //sets sum to 8192
(KBDCHECK)
	@KBD
	D=M //sets D to KBD input
	@BLACK
	D;JGT //runs BLACK if there is input
	@WHITE
	D;JEQ //runs WHITE if there is no input
	
(BLACK)
	@i
	D=M //sets i to D
	@SCREEN
	A=A+D //sets address to SCREEN + i
	M=-1 //sets current register to black
	@INC
	A;JMP //jumps to INC
	
(WHITE)
	@i
	D=M //sets i to D
	@SCREEN
	A=A+D //sets address to SCREEN + i
	M=0 //sets current register to white
	@INC
	A;JMP //jumps to INC
	
(INC)
	@i
	M=M+1 //increments i by 1 to cover the next register
	@sum
	D=M-D 
	@RESET
	D;JEQ //jumps to RESET if i=max
	@KBDCHECK
	A;JMP //jumps to KBDCHECK
```
## Notes
- Somewhat referred to a solution but still found my own method
- Surprised at how well I was able to adapt to assembly
	- Should probably work on commenting skills though
- 33 lines, people were able to make it 18 :eyes:
	- Not bad considering it's my first iteration
___