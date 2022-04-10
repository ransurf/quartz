---
title: Inc16
---
Status:
Links: [Nand2Tetris Project 2](out/nand2tetris-project-2.md)
___
# Inc16 Gate
## Notes
- Notes

## Code
```
CHIP Inc16 {
    IN in[16];
    OUT out[16];

    PARTS:
	Add16(a[0..15]=in[0..15], b[0]=true, b[1..15]=false, out[0..15]=out);
}
```
## Truth Table
| in               | out              |
| ---------------- | ---------------- |
| 0000000000000000 | 0000000000000001 |
| 1111111111111111 | 0000000000000000 |
| 0000000000000101 | 0000000000000110 |
| 1111111111111011 | 1111111111111100 |

___