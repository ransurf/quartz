---
title: RAM64
---
Status:
Links: [Nand2Tetris Project 3](out/nand2tetris-project-3.md)
___
#  RAM64
## Notes
- First half of the address was for choosing the right ram, the second half was for choosing the right register in the ram
- Didn't need to search up the solution to this one :D

## Code
```
CHIP RAM64 {
    IN in[16], load, address[6];
    OUT out[16];

    PARTS:
    DMux8Way(in=load, sel[0..2]=address[3..5], a=r0, b=r1, c=r2, d=r3, e=r4, f=r5, g=r6, h=r7);
    RAM8(in=in, load=r0, address=address[0..2], out=reg0);
	RAM8(in=in, load=r1, address=address[0..2], out=reg1);
	RAM8(in=in, load=r2, address=address[0..2], out=reg2);
	RAM8(in=in, load=r3, address=address[0..2], out=reg3);
	RAM8(in=in, load=r4, address=address[0..2], out=reg4);
	RAM8(in=in, load=r5, address=address[0..2], out=reg5);
	RAM8(in=in, load=r6, address=address[0..2], out=reg6);
	RAM8(in=in, load=r7, address=address[0..2], out=reg7);
	Mux8Way16(a=reg0, b=reg1, c=reg2, d=reg3, e=reg4, f=reg5, g=reg6, h=reg7, sel=address[3..5], out=out);
}
```
## Truth Table

| time | in   | load | address | out  |
| ---- | ---- | ---- | ------- | ---- |
| 0+   | 0    | 0    | 0       | 0    |
| 1    | 0    | 0    | 0       | 0    |
| 1+   | 0    | 1    | 0       | 0    |
| 2    | 0    | 1    | 0       | 0    |
| 2+   | 1313 | 0    | 0       | 0    |
| 3    | 1313 | 0    | 0       | 0    |
| 3+   | 1313 | 1    | 13      | 0    |
| 4    | 1313 | 1    | 13      | 1313 |
| 4+   | 1313 | 0    | 0       | 0    |
| 5    | 1313 | 0    | 0       | 0    |
| 5+   | 4747 | 0    | 47      | 0    |
| 6    | 4747 | 0    | 47      | 0    |
| 6+   | 4747 | 1    | 47      | 0    |
| 7    | 4747 | 1    | 47      | 4747 |
| 7+   | 4747 | 0    | 47      | 4747 |
| 8    | 4747 | 0    | 47      | 4747 |
| 8    | 4747 | 0    | 13      | 1313 |
| 8+   | 6363 | 0    | 13      | 1313 |
| 9    | 6363 | 0    | 13      | 1313 |
| 9+   | 6363 | 1    | 63      | 0    |
___