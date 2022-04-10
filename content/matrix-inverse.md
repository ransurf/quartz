---
title: Matrix Inverse
aliases:
---
Status:
Tags: #cards/math232/unit3
Links: [Matrix](out/matrix.md)
___

# Matrix Inverse

## Principles
?
- Not all matrices have an inverse
- Matrix inverses are unique

### General form for 2x2
?
- ad - bc != 0 is deteriminant
- If ad-bc = 0 then no inverse
- [![Image from Gyazo](https://i.gyazo.com/f09e46a83d371b56b55a22d8cb10f351.png)](https://gyazo.com/f09e46a83d371b56b55a22d8cb10f351)
- Turns A to I
- Turns I to $A^{-1}$
<!--SR:!2022-03-05,2,130-->

### In relation to matrix A and B
?
If A is a matrix and B is a matrix such that AB = I, then B is inverse of A, denoted $A^{-1}$
- I is standard basis matrix / multiplicative matrix
<!--SR:!2022-03-05,2,130-->

### Properties
[![Image from Gyazo](https://i.gyazo.com/c8d146ac6ef953000b50f191b7eaab34.png)](https://gyazo.com/c8d146ac6ef953000b50f191b7eaab34)
[![Image from Gyazo](https://i.gyazo.com/c554c14f701b28be8854a3618fac9305.png)](https://gyazo.com/c554c14f701b28be8854a3618fac9305)

### Finding general form for matrix inverse
[![Image from Gyazo](https://i.gyazo.com/684e8a70ce01f021285aed978e36a5ff.png)](https://gyazo.com/684e8a70ce01f021285aed978e36a5ff)
?
- Solve for
	- [![Image from Gyazo](https://i.gyazo.com/75a3a6059c13c10b19413865143dd4e0.png)](https://gyazo.com/75a3a6059c13c10b19413865143dd4e0)
- Distribute using matrix multiplication to create a system for each column in x
- you can use letter variables as a scalar
- [![Image from Gyazo](https://i.gyazo.com/e59f54513241cd53ad21dbf4700d9d85.png)](https://gyazo.com/e59f54513241cd53ad21dbf4700d9d85)
[![Image from Gyazo](https://i.gyazo.com/f09e46a83d371b56b55a22d8cb10f351.png)](https://gyazo.com/f09e46a83d371b56b55a22d8cb10f351)

### Invertible Matrix Theorem
?
[![Image from Gyazo](https://i.gyazo.com/221eb73bebe08cb137c15a1a0c3b542e.png)](https://gyazo.com/221eb73bebe08cb137c15a1a0c3b542e)

### Inverse Linear Mappings
[![Image from Gyazo](https://i.gyazo.com/5e2c5c38e96fd420751213c2950dccea.png)](https://gyazo.com/5e2c5c38e96fd420751213c2950dccea)
?
- If you have the inverse of the matrix, you can find the inverse linear mapping
- [![Image from Gyazo](https://i.gyazo.com/b0935382c1f80b0a97db683f446317df.png)](https://gyazo.com/b0935382c1f80b0a97db683f446317df)
- Inverse maps
- [![Image from Gyazo](https://i.gyazo.com/ca0cc2155095345584d59d933e34a9b5.png)](https://gyazo.com/ca0cc2155095345584d59d933e34a9b5)
<!--SR:!2022-02-13,2,150-->

## Examples
[![Image from Gyazo](https://i.gyazo.com/864b5023f9f28b221cd0a85748c35ab8.png)](https://gyazo.com/864b5023f9f28b221cd0a85748c35ab8)
?
- Turn LHS into identity matrix, right will be inverse
- [![Image from Gyazo](https://i.gyazo.com/dc8e1d2b7f70d7eaa7902fff7c0a99b1.png)](https://gyazo.com/dc8e1d2b7f70d7eaa7902fff7c0a99b1)
- Check by A(B) = I?
[![Image from Gyazo](https://i.gyazo.com/70c4dcb542b27488f134c65aeadfb5c3.png)](https://gyazo.com/70c4dcb542b27488f134c65aeadfb5c3)
### Find x in for AX=B
[![Image from Gyazo](https://i.gyazo.com/ebd2165571119bdaa0fa466198a5ce4d.png)](https://gyazo.com/ebd2165571119bdaa0fa466198a5ce4d)

### Find x in for XA=B
X = B$A^{-1}$
___

# Backlinks
```dataview
list from [Matrix Inverse](out/matrix-inverse.md) AND !outgoing([Matrix Inverse](out/matrix-inverse.md))
```
___
References:

Created:: 2022-02-05 17:53
