Status:
Links: [[Computer Gates]]
# DMux Gate
## Notes
- Took me a long time to figure out lmao
	- a will only be 1 if in is 1 and sel is 0, so you have to have the [[Not Gate]] of sel as input
	- b will only be 1 if both are one, so just use [[And Gate]]
```
CHIP DMux {
	IN in, sel;
	OUT a, b;

	PARTS:
	Not(in=sel, out=notSel);
	And(a=in, b=notSel, out=a);
	And(a=in, b=sel, out=b);
}
```
### Truth Table

in|sel|a|b
--|--|--|--
0|0|0|0
0|1|0|0
1|0|1|0
1|1|0|1
___