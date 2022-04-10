---
title: Not Gate
---
Links: [Computer Gates](out/computer-gates.md)
___
# Not Gate
## Notes
- Since a and b are the same, it will always be the same as the input given

## Code
``` /**
 * Not gate:
 * out = not in
 */

CHIP Not {
    IN in;
    OUT out;

    PARTS:
    Nand(a=in, b=in, out=out);
} 
```
___