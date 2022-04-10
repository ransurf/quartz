Status:
Tags:
Links: [[Flip Flops]] - [[Nand2Tetris Project 3]]
___
# Bit Register
## Notes
`if load (t-1) then out(t)=in(t-1) else out(t)=out(t-1)`
- Only changes output when load is 1
- Uses a DFF and mux with the output being refed into the mux
- Can be expanded, with w=word width
## Code
```
CHIP Register {
    IN in[16], load;
    OUT out[16];

    PARTS:
    Bit(in=in[0], load=load, out=out[0]);
	Bit(in=in[1], load=load, out=out[1]);
	Bit(in=in[2], load=load, out=out[2]);
	Bit(in=in[3], load=load, out=out[3]);
	Bit(in=in[4], load=load, out=out[4]);
	Bit(in=in[5], load=load, out=out[5]);
	Bit(in=in[6], load=load, out=out[6]);
	Bit(in=in[7], load=load, out=out[7]);
	Bit(in=in[8], load=load, out=out[8]);
	Bit(in=in[9], load=load, out=out[9]);
	Bit(in=in[10], load=load, out=out[10]);
	Bit(in=in[11], load=load, out=out[11]);
	Bit(in=in[12], load=load, out=out[12]);
	Bit(in=in[13], load=load, out=out[13]);
	Bit(in=in[14], load=load, out=out[14]);
	Bit(in=in[15], load=load, out=out[15]);
}
```
## Example Truth Table
![[1 bit register.png]]

| time | in     | load | out    |
| ---- | ------ | ---- | ------ |
| 0+   | 0      | 0    | 0      | 
| 1    | 0      | 0    | 0      |
| 1+   | 0      | 1    | 0      |
| 2    | 0      | 1    | 0      |
| 2+   | -32123 | 0    | 0      |
| 3    | -32123 | 0    | 0      |
| 3+   | 11111  | 0    | 0      |
| 4    | 11111  | 0    | 0      |
| 4+   | -32123 | 1    | 0      |
| 5    | -32123 | 1    | -32123 |
| 5+   | -32123 | 1    | -32123 |
| 6    | -32123 | 1    | -32123 |
| 6+   | -32123 | 0    | -32123 |
| 7    | -32123 | 0    | -32123 |
| 7+   | 12345  | 1    | -32123 |
| 8    | 12345  | 1    | 12345  |
| 8+   | 0      | 0    | 12345  |
| 9    | 0      | 0    | 12345  |
| 9+   | 0      | 1    | 12345  |
| 10   | 0      | 1    | 0      |
#### Terms
**Register State** - the current state stored in the register
___
References: