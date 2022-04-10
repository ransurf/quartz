---
title: Method of Least Squares
aliases:
---
Status:
Tags: #cards/math232/unit7/3
Links: [Subspace Projections](out/subspace-projections.md)
___

# Method of Least Squares

## Principles
Usual formula for quadratics
?
[![Image from Gyazo](https://i.gyazo.com/26188e5839905d898710175f71617480.png)](https://gyazo.com/26188e5839905d898710175f71617480)
- X is derived from the design matrix, whatever the polynomial equation is
- a is a,b,c
- y is y values given

When is $X^TX$ invertible
?
- When number of $t_i$ values >= number of unknown coefficients
- [![Image from Gyazo](https://i.gyazo.com/f952a22c47d0d0745acf3fc08e75a45c.png)](https://gyazo.com/f952a22c47d0d0745acf3fc08e75a45c)
- Produces a unique solution


### Overdetermined systems
?
- When a system has more equations than unknowns
- If no x such that Ax = b, find a vector x that minimizes the error ||Ax-b||
- This satisfies the normal system $A^TA\vec{x} = A^T\vec{b}$


## Examples
[![Image from Gyazo](https://i.gyazo.com/bdc118d683d23b508daca3d9ae3f656d.png)](https://gyazo.com/bdc118d683d23b508daca3d9ae3f656d)
?
[![Image from Gyazo](https://i.gyazo.com/61e1466baf64899e1f304f6121215ba4.png)](https://gyazo.com/61e1466baf64899e1f304f6121215ba4)
- a always 1

[![Image from Gyazo](https://i.gyazo.com/48564ccffbc08c7158963b31d7ab048b.png)](https://gyazo.com/48564ccffbc08c7158963b31d7ab048b)
?
[![Image from Gyazo](https://i.gyazo.com/75ea9171f84bf24f73e31c5360dbe16d.png)](https://gyazo.com/75ea9171f84bf24f73e31c5360dbe16d)


[![Image from Gyazo](https://i.gyazo.com/cb1c83df993f9726082bec7aeeba6fed.png)](https://gyazo.com/cb1c83df993f9726082bec7aeeba6fed)
?
[![Image from Gyazo](https://i.gyazo.com/6f02507aa1a1e908c660dc356f66f8a8.png)](https://gyazo.com/6f02507aa1a1e908c660dc356f66f8a8)

___
References:

Created:: 2022-03-30 00:44
