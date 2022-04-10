---
title: Xor Gate
---
[Computer Gates](out/computer-gates.md)
[Nand2Tetris Project 1](out/nand2tetris-project-1.md)
#  Gate
```
CHIP Xor {
    IN a, b;
    OUT out;

    PARTS:
    Not(in=a, out=NotA);
	Not(in=b, out=NotB);
	Nand(a=NotA, b=NotB, out=NandOut1);
	Nand(a=a, b=b, out=NandOut2);
	And(a=NandOut1, b=NandOut2, out=out);
}
```
### Truth Table

a | b | out
-- | -- | --
 0|0|0
 0|1|1
 1|0|1
 1|1|0

### Notes
- Could maybe be more convenient but w/e