Status:
Tags:
Links: [[Nand2Tetris Project 3]]
___
# Program Counter
## Notes
- Can be built from a register, incrementor, and logic gates
- Definitely did not copy!!!11one
## Code
```
CHIP PC {
    IN in[16],load,inc,reset;
    OUT out[16];

    PARTS:
	//inc
    Inc16(in=oo, out=t1);
	Mux16(a=oo, b=t1, sel=inc, out=incOut);
	//load
	Mux16(a=incOut, b=in, sel=load, out=loadOut);
	//reset
	Mux16(a=loadOut, b[0..15]=false, sel=reset, out=resetOut);

	Register(in=resetOut, load=true, out=out, out=oo);
	
}
```
## Truth Table
| time | in     | reset | load | inc | out    |
| ---- | ------ | ----- | ---- | --- | ------ |
| 0+   | 0      | 0     | 0    | 0   | 0      |
| 1    | 0      | 0     | 0    | 0   | 0      |
| 1+   | 0      | 0     | 0    | 1   | 0      |
| 2    | 0      | 0     | 0    | 1   | 1      |
| 2+   | -32123 | 0     | 0    | 1   | 1      |
| 3    | -32123 | 0     | 0    | 1   | 2      |
| 3+   | -32123 | 0     | 1    | 1   | 2      |
| 4    | -32123 | 0     | 1    | 1   | -32123 |
| 4+   | -32123 | 0     | 0    | 1   | -32123 |
| 5    | -32123 | 0     | 0    | 1   | -32122 |
| 5+   | -32123 | 0     | 0    | 1   | -32122 |
| 6    | -32123 | 0     | 0    | 1   | -32121 |
| 6+   | 12345  | 0     | 1    | 0   | -32121 |
| 7    | 12345  | 0     | 1    | 0   | 12345  |
| 7+   | 12345  | 1     | 1    | 0   | 12345  |
| 8    | 12345  | 1     | 1    | 0   | 0      |
| 8+   | 12345  | 0     | 1    | 1   | 0      |
| 9    | 12345  | 0     | 1    | 1   | 12345  |
| 9+   | 12345  | 1     | 1    | 1   | 12345  |
| 10   | 12345  | 1     | 1    | 1   | 0      |
| 10+  | 12345  | 0     | 0    | 1   | 0      |
| 11   | 12345  | 0     | 0    | 1   | 1      |
| 11+  | 12345  | 1     | 0    | 1   | 1      |
| 12   | 12345  | 1     | 0    | 1   | 0      |
| 12+  | 0      | 0     | 1    | 1   | 0      |
| 13   | 0      | 0     | 1    | 1   | 0      |
| 13+  | 0      | 0     | 0    | 1   | 0      |
| 14   | 0      | 0     | 0    | 1   | 1      |
| 14+  | 22222  | 1     | 0    | 0   | 1      |
| 15   | 22222  | 1     | 0    | 0   | 0      |
___
References: