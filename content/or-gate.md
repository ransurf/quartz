---
title: Or Gate
---
[Computer Gates](out/computer-gates.md)
[Nand2Tetris Project 1](out/nand2tetris-project-1.md)
#  Or Gate
### Notes
- Outputs 1 if a or b is 1
### Code
```
CHIP Or {
    IN a, b;
    OUT out;

    PARTS:
    Not(in=a, out=NotA);
	Not(in=b, out=NotB);
	Nand(a=NotA, b=NotB, out=out);
}
```
### Truth Table

a | b | out
-- | -- | --
 0|0|0
 0|1|1
 1|0|1
 1|1|1
