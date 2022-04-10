---
title: DMux8Way Gate
---
Status:
Links: [Computer Gates](out/computer-gates.md)
___
# DMux8Way Gate
## Notes
- Was low on time so I searched them up; I just gotta let it sink in for me to understand
- 

## Code
```
CHIP DMux8Way {
    IN in, sel[3];
    OUT a, b, c, d, e, f, g, h;

    PARTS:
	DMux(in=in, sel=sel[2], a=dmux1, b=dmux2);
    DMux4Way(in=dmux1, sel[0..1]=sel[0..1], a=a, b=b, c=c, d=d);
	DMux4Way(in=dmux2, sel[0..1]=sel[0..1], a=e, b=f, c=g, d=h);
	
}
```
## Truth Table
- Refer to [DMux4Way Gate](out/dmux4way-gate.md)
___