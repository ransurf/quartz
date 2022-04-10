Status:
Tags:
Links: [[Nand2Tetris Unit 6]]
___
# Assembler Logic
## Process
- Read the next Assembly language command
- Break it into different fields ([[Parsing]])
- Lookup binary code for each field
- Combine codes into a single machine language command
- Output machine language command
Does the following process until the end of the file is reached
### Treatment of Code Parts
- Whitespace
	- Ignore
- Instructions
	- Converts into binary
- Symbols
	1. Pre-defined
		- Only a instructions
		- Replace symbol with value
	2. Labels `(label)`
		- `label` will turn into the memory location value of the next instruction
		- `@label` turns into `@value`
	3. Variables `@var`
		- If `@var` is not used in parentheses, it becomes a variable
		- Given a unique memory address starting at 16, and refer to it for further occasions of the naem
## Symbols
### Types
- Pre-defined symbols
- Labels
	- Runs through the code initially to map all addresses
	-	ex) JMP loop
- Variables
	- ex) Load R1, weight
### Process
- Stored in a [[Symbol Table]]
___
References: