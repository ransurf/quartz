Status:
Tags:
Links: [[Nand2Tetris Unit 5]]
___
# Nand2Tetris Project 5
[Link to Website](https://www.nand2tetris.org/project05)
[Instruction Bits Powerpoint](https://docs.wixstatic.com/ugd/56440f_96cbb9c6b8b84760a04c369453b62908.pdf)
## Memory
- [[HACK Memory Implementation]]
### Tips
- Realize the abstraction
	- RAM, Screen, Keyboard
	- Funnels into correct register
## CPU
- [[HACK CPU Implementation]]
### Tips
- All chips are made from previous parts
- C fields are from instructions
	- Use HDL to send route instruction bits to the control bits of relevant chip-parts
- Used proposed implementation in figure 5.9 of chapter 5
	- Use ARegister and DRegister for extra GUI side-effects
- Load of PC should be a comparison of jump bits and output of number
	- j1 is < 0
	- j2 is = 0
	- j3 is > 0
## ROM
- Free real estate B)
- Implemented using ROM32K chip
## Computer
- [[HACK Computer Implementation]]
___
References: