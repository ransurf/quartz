---
title: RAM4K
---
Status:
Links: [Nand2Tetris Project 3](out/nand2tetris-project-3.md)
___
#  
## Notes
- Notes

## Code
```
CHIP RAM4K {
    IN in[16], load, address[12];
    OUT out[16];

    PARTS:
    DMux8Way(in=load, sel[0..2]=address[9..11], a=r0, b=r1, c=r2, d=r3, e=r4, f=r5, g=r6, h=r7);
    RAM512(in=in, load=r0, address=address[0..8], out=reg0);
	RAM512(in=in, load=r1, address=address[0..8], out=reg1);
	RAM512(in=in, load=r2, address=address[0..8], out=reg2);
	RAM512(in=in, load=r3, address=address[0..8], out=reg3);
	RAM512(in=in, load=r4, address=address[0..8], out=reg4);
	RAM512(in=in, load=r5, address=address[0..8], out=reg5);
	RAM512(in=in, load=r6, address=address[0..8], out=reg6);
	RAM512(in=in, load=r7, address=address[0..8], out=reg7);
	Mux8Way16(a=reg0, b=reg1, c=reg2, d=reg3, e=reg4, f=reg5, g=reg6, h=reg7, sel=address[9..11], out=out);
}
```
## Truth Table

| time | in   | load | address | out  |
| ---- | ---- | ---- | ------- | ---- |
| 0+   | 0    | 0    | 0       | 0    |
| 1    | 0    | 0    | 0       | 0    |
| 1+   | 0    | 1    | 0       | 0    |
| 2    | 0    | 1    | 0       | 0    |
| 2+   | 1111 | 0    | 0       | 0    |
| 3    | 1111 | 0    | 0       | 0    |
| 3+   | 1111 | 1    | 1111    | 0    |
| 4    | 1111 | 1    | 1111    | 1111 |
| 4+   | 1111 | 0    | 0       | 0    |
| 5    | 1111 | 0    | 0       | 0    |
| 5+   | 3513 | 0    | 3513    | 0    |
| 6    | 3513 | 0    | 3513    | 0    |
| 6+   | 3513 | 1    | 3513    | 0    |
| 7    | 3513 | 1    | 3513    | 3513 |
| 7+   | 3513 | 0    | 3513    | 3513 |
| 8    | 3513 | 0    | 3513    | 3513 |
| 8    | 3513 | 0    | 1111    | 1111 |
| 8+   | 4095 | 0    | 1111    | 1111 |
| 9    | 4095 | 0    | 1111    | 1111 |
| 9+   | 4095 | 1    | 4095    | 0    |
___