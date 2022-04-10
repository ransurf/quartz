Status:
Links: [[Nand2Tetris Project 2]]
___
#  Gate
## Notes
- Decided to search up the solution xd
- 

## Code
```
CHIP FullAdder {
    IN a, b, c;  // 1-bit inputs
    OUT sum,     // Right bit of a + b + c
        carry;   // Left bit of a + b + c

    PARTS:
	HalfAdder(a=a, b=b, sum=w1, carry=c1);
    HalfAdder(a=w1, b=c, sum=sum, carry=c2);
    Or(a=c1, b=c2, out=carry);
}
```
## Truth Table
| a   | b   | c   | sum | carry |
| --- | --- | --- | --- | ----- |
| 0   | 0   | 0   | 0   | 0     |
| 0   | 0   | 1   | 1   | 0     |
| 0   | 1   | 0   | 1   | 0     |
| 0   | 1   | 1   | 0   | 1     |
| 1   | 0   | 0   | 1   | 0     |
| 1   | 0   | 1   | 0   | 1     |
| 1   | 1   | 0   | 0   | 1     |
| 1   | 1   | 1   | 1   | 1     |
___