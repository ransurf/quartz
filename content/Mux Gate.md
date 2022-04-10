Links: [[Computer Gates]] - [[Nand2Tetris Project 1]]
# Mux Gate
### Notes
- outputs a if sel=0, b otherwise
### Code
```
CHIP Mux {
    IN a, b, sel;
    OUT out;

    PARTS:
	Not(in=sel, out=nandSel);
    And(a=a, b=nandSel, out=aAndSel);
	And(a=sel, b=b, out=bAndSel);
	Or(a=aAndSel, b=bAndSel, out=out);
	
}
```
### Truth Table

a|b|sel|out
--|--|--|--
 0|0|0|0
 0|1|0|0
 1|0|0|1
 1|1|0|1
 0|0|1|0
 0|1|1|1
 1|0|1|0
 1|1|1|1
