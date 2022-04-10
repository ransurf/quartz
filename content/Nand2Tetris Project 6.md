Status:
Tags:
Links: [[Nand2Tetris Unit 6]]
___
# Nand2Tetris Project 6
[Details Page](https://www.nand2tetris.org/project06)

## Goal
Create an assembler that translates assembly code into machine language
## Classes
### Parser
- Unpacks each instruction into its underlying fields
### Code
- Translates each field into its corresponding binary value
### SymbolTable
- Manages the symbol table
### Main
- Initializes I/O files, drives process
## Suggestions
### Development
1. Develop a basic assembler that works without symbols
	- Test it
2. Develop an ability to handle symbols
	- Test it
3. Morph into an assembler that can translate any assembly program
	- Refer to supplied test program
		- L = less symbols
### Testing
1. Use the assembler to translate .asm file into .hack
2. Load .hack into one of the following:
	- Hardware Simulator
	- CPU Emulator
	- Assembler
		- Compare translated code into our own
___
References: