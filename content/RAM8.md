---
title: RAM8
---
Status:
Tags:
Links: [Nand2Tetris Project 3](out/nand2tetris-project-3.md)
___
# RAM8
## Notes
- Feed the in value to all the registers simultaneously
- use mux, demux logic to select the right register
- RAM's adress input consists of:
	- A field to select a ram part
	- A register within that ram part
## Code
```
CHIP RAM8 {
    IN in[16], load, address[3];
    OUT out[16];
	
    PARTS:
	DMux8Way(in=load, sel=address, a=l0, b=l1, c=l2, d=l3, e=l4, f=l5, g=l6, h=l7);
    Register(in=in, load=l0, out=reg0);
	Register(in=in, load=l1, out=reg1);
	Register(in=in, load=l2, out=reg2);
	Register(in=in, load=l3, out=reg3);
	Register(in=in, load=l4, out=reg4);
	Register(in=in, load=l5, out=reg5);
	Register(in=in, load=l6, out=reg6);
	Register(in=in, load=l7, out=reg7);
	Mux8Way16(a=reg0, b=reg1, c=reg2, d=reg3, e=reg4, f=reg5, g=reg6, h=reg7, sel=address, out=out);
}
```
## Truth Table

| time | in    | load | address | out   |
| ---- | ----- | ---- | ------- | ----- |
| 0+   | 0     | 0    | 0       | 0     |
| 1    | 0     | 0    | 0       | 0     |
| 1+   | 0     | 1    | 0       | 0     |
| 2    | 0     | 1    | 0       | 0     |
| 2+   | 11111 | 0    | 0       | 0     |
| 3    | 11111 | 0    | 0       | 0     |
| 3+   | 11111 | 1    | 1       | 0     |
| 4    | 11111 | 1    | 1       | 11111 |
| 4+   | 11111 | 0    | 0       | 0     |
| 5    | 11111 | 0    | 0       | 0     |
| 5+   | 3333  | 0    | 3       | 0     |
| 6    | 3333  | 0    | 3       | 0     |
| 6+   | 3333  | 1    | 3       | 0     |
| 7    | 3333  | 1    | 3       | 3333  |
| 7+   | 3333  | 0    | 3       | 3333  |
| 8    | 3333  | 0    | 3       | 3333  |
| 8    | 3333  | 0    | 1       | 11111 |
| 8+   | 7777  | 0    | 1       | 11111 |
| 9    | 7777  | 0    | 1       | 11111 |
| 9+   | 7777  | 1    | 7       | 0     |
___
References: