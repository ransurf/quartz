---
title: DMux4Way Gate
---
Status:
Links: [Computer Gates](out/computer-gates.md)
___
# DMux4Way Gate
## Notes
- Not 100% understanding on how it works
- c and d won't be able to have the input if sel[2] = 0, and a and b won't be able to have the input if sel[2]=1

## Code
```
CHIP DMux4Way {
    IN in, sel[2];
    OUT a, b, c, d;

    PARTS:
    DMux(in=in, sel=sel[1], a=t1, b=t2);
	DMux(in=t1, sel=sel[0], a=a, b=b);
	DMux(in=t2, sel=sel[0], a=c, b=d);
	
}
```
## Truth Table
in  | sel  |  a  |  b  |  c  |  d 
-- | -- | -- | -- | -- | --
0  |  00  |  0  |  0  |  0  |  0  
0  |  01  |  0  |  0  |  0  |  0  
0  |  10  |  0  |  0  |  0  |  0  
 0  |  11  |  0  |  0  |  0  |  0  
1  |  00  |  1  |  0  |  0  |  0  
1  |  01  |  0  |  1  |  0  |  0  
1  |  10  |  0  |  0  |  1  |  0  
1  |  11  |  0  |  0  |  0  |  1  
___