Links: [[Computer Gates]] - [[Nand2Tetris Project 1]]
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