**Status:
Tags:
Links: [[Nand2Tetris Project 4]]
___
# Nand2Tetris Mult Program
## Objective
- This program computes the value R0\*R1 and stores the result in R2.
## Ideas
- Use for loops to add R0 to R2 R1 times
## Psuedo-Code
```
n = R1
i = 0

LOOP:
	if i > n goto END
	R2 = R0 + R2 // set adress to R2 and data to R0, M = M + D
	i++
	goto LOOP
END:
	goto END

```
## ASM Code
```
@R1
D=M
@n
M=D //set n to R1

@i
M=0 //set i to 0

@r
M=0 //set r to 0

(LOOP)
	@i
	D=M
	@n
	D=D-M
	@END
	D;JEQ //if i>n goto END
	
	@R0
	D=M
	@END
	D;JEQ //sets R2 to 0 if R0 = 0
	
	@R1
	D=M
	@END
	D;JEQ //sets R2 to 0 if R1 = 0
	
	@R0
	D=M //set D to R0
	@r
	M=D+M //adds R0 to r
	
	@i
	M=M+1 //i = i+1
	
	@LOOP
	0;JMP //rerun loop
	
(END)
	@r
	D=M
	@R2
	M=D
	@END
	0;JMP //infinite loop
```
## Thoughts
- Could definitely be more optimized
	- I saw a solution had it where they used a while loop instead of a for loop
		- I just used the for loop since it was given as an example xd
- Super happy I was able to solve it independently
	- Using a new variable to mitigate the -1 set
	- Understanding that JGT should have been JEQ
___
References: