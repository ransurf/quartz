Status:
Links: [[Nand2Tetris Project 3]]
___
#  
## Notes
- Didn't follow same 8x growth as the other predecessors :(

## Code
```
CHIP RAM16K {
    IN in[16], load, address[14];
    OUT out[16];

    PARTS:
    DMux4Way(in=load, sel[0..1]=address[12..13], a=r0, b=r1, c=r2, d=r3);
    RAM4K(in=in, load=r0, address=address[0..11], out=reg0);
	RAM4K(in=in, load=r1, address=address[0..11], out=reg1);
	RAM4K(in=in, load=r2, address=address[0..11], out=reg2);
	RAM4K(in=in, load=r3, address=address[0..11], out=reg3);
	Mux4Way16(a=reg0, b=reg1, c=reg2, d=reg3, sel=address[12..13], out=out);
}
```
## Truth Table
| time | in    | load | address | out   |
| ---- | ----- | ---- | ------- | ----- |
| 0+   | 0     | 0    | 0       | 0     |
| 1    | 0     | 0    | 0       | 0     |
| 1+   | 0     | 1    | 0       | 0     |
| 2    | 0     | 1    | 0       | 0     |
| 2+   | 4321  | 0    | 0       | 0     |
| 3    | 4321  | 0    | 0       | 0     |
| 3+   | 4321  | 1    | 4321    | 0     |
| 4    | 4321  | 1    | 4321    | 4321  |
| 4+   | 4321  | 0    | 0       | 0     |
| 5    | 4321  | 0    | 0       | 0     |
| 5+   | 12345 | 0    | 12345   | 0     |
| 6    | 12345 | 0    | 12345   | 0     |
| 6+   | 12345 | 1    | 12345   | 0     |
| 7    | 12345 | 1    | 12345   | 12345 |
| 7+   | 12345 | 0    | 12345   | 12345 |
| 8    | 12345 | 0    | 12345   | 12345 |
| 8    | 12345 | 0    | 4321    | 4321  |
| 8+   | 16383 | 0    | 4321    | 4321  |
| 9    | 16383 | 0    | 4321    | 4321  |
| 9+   | 16383 | 1    | 16383   | 0     |
___