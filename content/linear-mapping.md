---
title: Linear Mapping
aliases:
---
 Status:
Tags: #cards/math232/unit3 #cards/math232/unit4
Links: [Vector Line Equations](out/vector-line-equations.md)
___

# Linear Mapping

## Principles
?
Ø = some transformation $R^n$ -> $R^n$
- Ø(kx) = kØ(x)
	- linear with respect to scalar product
- Ø(x+y) = Ø(x) + Ø(y)
	- linear wrt vector addition
<!--SR:!2022-03-28,6,130-->

Linear operators
?
- Linear mappings but dimensions stay the same
<!--SR:!2022-04-02,11,152-->

Checking if a vector is in a range of a linear mapping
?
- Create liner system with x components = y components
- RREF
- In range if consistent, RHS is the x vector such that L(x) = y
<!--SR:!2022-03-28,3,130-->

### Types
Zero mapping as a linear operator
?
- Z(v) = 0w for all v in V
<!--SR:!2022-03-31,6,150-->

Identity mapping as a linear operator
?
- Maps to itself
<!--SR:!2022-04-08,14,150-->

Nullsp

### Checking
Check if you can turn Ø(tx+sy) = tØ(x) + sØ(y)
- Apply t, s, etc to the preimage, then substitute those expanded components into the image
- Need to find form tL($\vec{x}$) + sL($\vec{y}$)

### Rules
- For any linear mapping, Ø, Ø(0 vector) = 0
	- since k=0 would set everything to 0
- No constant terms/homogeneous
- No exponents
- Mapping is linear iff it is a matrix mapping

## Examples
Determine if the following mappings are linear and express them as a matrix mapping
[![Image from Gyazo](https://i.gyazo.com/b885142b6c08f5d5a58db561173409fb.png)](https://gyazo.com/b885142b6c08f5d5a58db561173409fb)
?
[![Image from Gyazo](https://i.gyazo.com/2558a742cca6d140d7c96cb6f414746e.png)](https://gyazo.com/2558a742cca6d140d7c96cb6f414746e)
- Ø(tx+sy) => tØ(x) + sØ(y) where t and s are just generic scalars
- work towards that general solution
- first step is scalar multiplication
- next is vector addition, end up with the different components
- apply the transformation onto the respective components
- expand
- gcf t and s, factor out the equation and you're left with the LHS
<!--SR:!2022-03-28,3,130-->

[![Image from Gyazo](https://i.gyazo.com/76c1d0642e4965000a85a4a63ddaafc2.jpg)](https://gyazo.com/76c1d0642e4965000a85a4a63ddaafc2)

[![Image from Gyazo](https://i.gyazo.com/d02c2dc0200cde69fa77818f3ccbc25b.png)](https://gyazo.com/d02c2dc0200cde69fa77818f3ccbc25b)
?
- L(s(x) + t(y)) = sL(x) + tL(y)
- Distribute s and t, combine into one matrix
- Plug into image
- GCF s, end up with the image ?
[![Image from Gyazo](https://i.gyazo.com/5c15dd357696be8e787300185cd46281.png)](https://gyazo.com/5c15dd357696be8e787300185cd46281)
<!--SR:!2022-03-26,4,130-->

[![Image from Gyazo](https://i.gyazo.com/17de00c8298a81045abfd4a83a123e5c.png)](https://gyazo.com/17de00c8298a81045abfd4a83a123e5c)

___

# Backlinks
```dataview
list from [Linear Mapping](out/linear-mapping.md) AND !outgoing([Linear Mapping](out/linear-mapping.md))
```
___
References:

Created:: 2022-01-28 21:06
