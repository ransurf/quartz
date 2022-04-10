---
title: Vector Coordinates
aliases:
---
Status:
Tags: #cards/math232/unit4
Links: [MATH 232 Units](out/math-232-units.md)
___

# Vector Coordinates

## Principles
?
- Coordinates ;; how much of each basis vector is in b
<!--SR:!2022-03-26,10,138-->
- Notation of basis of standard unit vectors ;; $B_o$
<!--SR:!2022-03-30,5,150-->
- (w)$B_o$ = ;; w
<!--SR:!2022-03-28,12,150-->

B as a set vs B as a matrix
?
[![Image from Gyazo](https://i.gyazo.com/8eceee62dc808a348207adfb7ea26da7.png)](https://gyazo.com/8eceee62dc808a348207adfb7ea26da7)
<!--SR:!2022-03-26,10,152-->

Textbook Definition
?
[![Image from Gyazo](https://i.gyazo.com/46d74d05542414311ba65fc19142682a.png)](https://gyazo.com/46d74d05542414311ba65fc19142682a)
<!--SR:!2022-04-01,10,150-->

System of linear equations in matrix form
?
Bc = w, where B is basis vectors and c is constants
<!--SR:!2022-03-26,1,130-->

Find coordinates of a vector wrt a basis
?
- Set each vector of basis as a column, RHS will be the components of vector
- RREF
- 
<!--SR:!2022-03-28,6,133-->

### Theorem
Change of coordinates
?
[![Image from Gyazo](https://i.gyazo.com/d068b2a55a6fb93149f917a16ffa83b4.png)](https://gyazo.com/d068b2a55a6fb93149f917a16ffa83b4)
<!--SR:!2022-03-26,1,130-->

Change of coordinates matrix
?
[![Image from Gyazo](https://i.gyazo.com/20f2eeba86480c846d980ec099b2d134.png)](https://gyazo.com/20f2eeba86480c846d980ec099b2d134)
<!--SR:!2022-03-26,1,130-->

Let B = basis and S = standard basis.
Change of coordinates matrix Q for B -> S and matrix P for S -> B
?
- Q = B -> S would just be B
- P = S -> B would equal the RREF of B in LHS and S in RHS
<!--SR:!2022-03-29,13,153-->


How to find change of coordinates matrix q from b-coord to c-coord, and the change of coordinates matrix p from c-coords to b-coords. verify pq = i
- 

## Examples
Find coordinates of v=(0,3) wrt basis B = {v1,v2}, v1=(2,1) and v2=(-1,1)
?
- I think bottom right component should be 1, pyke moment
- Each vector is a column, RREF and find valule sof each c
[![Image from Gyazo](https://i.gyazo.com/f871fd17fbbfb9fe96ccec10f04921a2.png)](https://gyazo.com/f871fd17fbbfb9fe96ccec10f04921a2)
<!--SR:!2022-03-27,11,153-->

Convert coordinate vector of p(x) = 4 + x wrt to basis B = {-1 + 2x, 1 + x}
?
- Write p as linear combination of basis vectors in B
- Setup linear combination, distrivute and regroup
- [![Image from Gyazo](https://i.gyazo.com/8d97260f55432fda2b1777e57de90d47.png)](https://gyazo.com/8d97260f55432fda2b1777e57de90d47)
- Plug into matrix, RHS = p(x) ?
- [![Image from Gyazo](https://i.gyazo.com/db262c2ecbe6022d23bb35de49964c09.png)](https://gyazo.com/db262c2ecbe6022d23bb35de49964c09)
<!--SR:!2022-03-27,5,130-->

[![Image from Gyazo](https://i.gyazo.com/450bd79dbb4e79ea69292b8573cc97da.png)](https://gyazo.com/450bd79dbb4e79ea69292b8573cc97da)
?
[![Image from Gyazo](https://i.gyazo.com/70291928b8d904a482e83976c365de8a.png)](https://gyazo.com/70291928b8d904a482e83976c365de8a)
___
References:
<!--SR:!2022-03-27,11,153-->

Created:: 2022-02-20 20:33
