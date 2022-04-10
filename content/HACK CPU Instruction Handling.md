Status:
Tags:
Links: [[HACK CPU Instruction Handling]]
___
# HACK CPU Instruction Handling
## A Instruction
- Refer to [[A Instruction (CPU)]]
### Diagram
![[a instruction handling.png]]
### Steps
1. Decodes instruction into op-code + 15-bit value
2. Stores value in a-register
3. Outputs value
## C Instruction
- Refer to [[C Instruction (CPU)]]
### Diagram
![[c instruction handling.png]]
### Steps
1. Decodes instruction into:
	1. Op-code
	2. ALU control bits
	3. Destination load bits
	4. Jump bits
___
References: