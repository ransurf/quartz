Status:
Links: [[Nand2Tetris Project 2]]
___
# Half-Adder
## Notes
- sum value is found through an xor gate
- carry value is found through an and gate

## Code
```
CHIP HalfAdder {
    IN a, b;    // 1-bit inputs
    OUT sum,    // Right bit of a + b 
        carry;  // Left bit of a + b

    PARTS:
    Xor(a=a, b=b, out=sum);
	And(a=a, b=b, out=carry);
}
```
## Truth Table
| a   | b   | sum | carry |
| --- | --- | --- | ----- |
| 0   | 0   | 0   | 0     |
| 1   | 0   | 1   | 0     |
| 0   | 1   | 1   | 0     |
| 1   | 1   | 0   | 1     |
