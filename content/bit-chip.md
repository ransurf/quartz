---
title: Bit Chip
---
Status:
Tags:
Links: [Nand2Tetris Project 3](out/nand2tetris-project-3.md)
___
# Bit Chip
## Notes
- Uses Mux and DFF
## Code
```
CHIP Bit {
    IN in, load;
    OUT out;

    PARTS:
    Mux(a=t1, b=in, sel=load, out=m1);
	DFF(in=m1, out=t1, out=out);
}

```
## Truth Table
| time | in  | load | out |
| ---- | --- | ---- | --- |
| 0+   | 0   | 0    | 0   |
| 1    | 0   | 0    | 0   |
| 1+   | 0   | 1    | 0   |
| 2    | 0   | 1    | 0   |
| 2+   | 1   | 0    | 0   |
| 3    | 1   | 0    | 0   |
| 3+   | 1   | 1    | 0   |
| 4    | 1   | 1    | 1   |
| 4+   | 0   | 0    | 1   |
| 5    | 0   | 0    | 1   |
| 5+   | 1   | 0    | 1   |
| 6    | 1   | 0    | 1   |
| 6+   | 0   | 1    | 1   |
| 7    | 0   | 1    | 0   |
| 7+   | 1   | 1    | 0   |
___
References: