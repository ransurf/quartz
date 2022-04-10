---
title: Homogeneous linear system
aliases:
---
Status:
Tags: #cards/math232/unit2
Links: [System of linear equations](out/system-of-linear-equations.md)
___

# Homogeneous linear system

## Principles
?
- When each of its equations are homogeneous
	- Last column of augmented matrix consist of only zeros
	- $b_i$ = 0 where b is the LHS
<!--SR:!2022-03-11,29,190-->

Solutions of a homogeneous linear system
?
- Always has one solution, trivial solution when $x_i$ = 0 for all i
	- nontrivial solutions
- If there is one nontrivial solution, then there are infinite since applying a scalar to LHS will still equal 0
- Therefore, either only trivial or infinite solutions
	- [![Image from Gyazo](https://i.gyazo.com/13175d67587fa81393fc0713a435a00a.png)](https://gyazo.com/13175d67587fa81393fc0713a435a00a)
<!--SR:!2022-03-07,25,170-->

- Solution of a homogeneous is based on free variables
	- If there are some, isolate x1 and represent them as the free variables
	- If there are none, then solution is empty vector

### Solution Space
?
- Is a subspace, called solution space
- Since homo always has 0 as solution set, we can't just test it
- Closed under scalar mult due to homogeneous nature
- Closed under vector addition
[![Image from Gyazo](https://i.gyazo.com/c25a35f25fb871383286e31332b16675.png)](https://gyazo.com/c25a35f25fb871383286e31332b16675)
<!--SR:!2022-02-20,10,130-->

To find solution/basis, move free variables to RHS and find the vector equation

Dimensions is number of free variables
## Questions

Find a homogeneous system that defines the given subspace
- 2.3 B4-11
?
- RREF, back substitution
___
<!--SR:!2022-02-13,2,160-->

# Backlinks
```dataview
list from [Homogeneous linear system](out/homogeneous-linear-system.md) AND !outgoing([Homogeneous linear system](out/homogeneous-linear-system.md))
```
___
References:

Created:: 2022-01-22 13:59
