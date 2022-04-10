Status:
Links: [[Nand2Tetris Project 5]]
___
# HACK Memory Implementation
## Notes
- RAM16k for storage, SCREEN (8k) for information, and keyboard
- Surprised I was able to get the theory and implementation of it, only problem was that I didn't know much about the kbd chip and had to search it up
	- Should've known it was out only lul

## Code
```
CHIP Memory {
    IN in[16], load, address[15];
    OUT out[16];

    PARTS:
	DMux4Way(in=load, sel=address[13..14], a=ramLoad0, b=ramLoad1, c=screenLoad, d=kbdLoad);
	Or(a=ramLoad0, b=ramLoad1, out=ramLoad2);
	RAM16K(in=in, load=ramLoad2, address=address[0..13], out=ramOut);
	Screen(in=in, load=screenLoad, address=address[0..12], out=screenOut);
	Keyboard(out=kbdOut);
	Mux4Way16(a=ramOut, b=ramOut, c=screenOut, d=kbdOut, sel=address[13..14], out=out);
}
```
## Truth Table
| in    | load | address         | out   |
| ----- | ---- | --------------- | ----- |
| 12345 | 1    | 010000000000000 | 0     |
| 12345 | 1    | 010000000000000 | 12345 |
| 12345 | 1    | 100000000000000 | 0     |
| 12345 | 1    | 100000000000000 | 12345 |
| -1    | 1    | 000000000000000 | 0     |
| -1    | 1    | 000000000000000 | -1    |
| 9999  | 0    | 000000000000000 | -1    |
| 9999  | 0    | 000000000000000 | -1    |
| 9999  | 0    | 010000000000000 | 12345 |
| 9999  | 0    | 100000000000000 | 12345 |
| 12345 | 1    | 000000000000000 | -1    |

___