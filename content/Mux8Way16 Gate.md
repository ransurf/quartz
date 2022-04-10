Status:
Links: [[Computer Gates]]
___
# Mux8Way16 Gate
## Notes
- Notes

## Code
```
CHIP Mux8Way16 {
    IN a[16], b[16], c[16], d[16],
       e[16], f[16], g[16], h[16],
       sel[3];
    OUT out[16];

    PARTS:
    Mux4Way16(a[0..15]=a[0..15], b[0..15]=b[0..15], c[0..15]=c[0..15], d[0..15]=d[0..15],sel[0..1]=sel[0..1], out[0..15]=abcdMux);
	Mux4Way16(a[0..15]=e[0..15], b[0..15]=f[0..15], c[0..15]=g[0..15], d[0..15]=h[0..15],sel[0..1]=sel[0..1], out[0..15]=efghMux);
	Mux16(a[0..15]=abcdMux, b[0..15]=efghMux, sel=sel[2], out[0..15]=out);
}
```
## Truth Table
Refer to [[Mux4Way16 Gate]] truth table
___