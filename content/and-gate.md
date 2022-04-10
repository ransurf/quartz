---
title: And Gate
---
Links: [Computer Gates](out/computer-gates.md) - [Nand2Tetris Project 1](out/nand2tetris-project-1.md)
# And Gate
```
CHIP And {
    IN a, b;
    OUT out;

    PARTS:
    Nand(a=a, b=b, out=NandOut);
	Not(in=NandOut, out=out);
}
```
### Truth Table

a | b | out
-- | -- | --
 0|0|0
 0|1|0
 1|0|0
 1|1|1

### Notes
- 