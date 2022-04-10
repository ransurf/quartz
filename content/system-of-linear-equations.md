---
title: System of linear equations
aliases: linear system
---
Status:
Tags: #cards/math232/unit2
Links: [Vector Line Equations](out/vector-line-equations.md)
___

# System of linear equations
- [System of linear equations applications](out/system-of-linear-equations-applications.md)
## Principles
?
[![Image from Gyazo](https://i.gyazo.com/209b50e43cbb909696219fedc1bb124d.png)](https://gyazo.com/209b50e43cbb909696219fedc1bb124d)
- Every linear system can have how many solutions ;; 0,1,infinity
<!--SR:!2022-03-10,28,190-->
### To vector form
- Multiply c scalars into vector, then turn into RREF
[![Image from Gyazo](https://i.gyazo.com/45fab683d47571b1f4811df6046bd807.png)](https://gyazo.com/45fab683d47571b1f4811df6046bd807)
### Types
- [Homogeneous linear system](out/homogeneous-linear-system.md)

## Solution Sets
- 2 equations of planes (x,y,z)
	- Solution set is a line if they intersect

## Solving
Steps
?
- Convert into [Augmented Matrix](out/augmented-matrix.md)
- Row operations
- RREF
- Identify leading variables (pivot columns)
- Identify [Free variables](out/free-variables.md)
- Write out solution set (infinite if 1+ free)
<!--SR:!2022-02-21,11,150-->

Various linear systems can have the same solution set, the goal of solving is by finding a more simpler matrix that we can easily find the solution of
- Even to the point where one of the variables is simply isolated
- Can be simplified using an [Augmented Matrix](out/augmented-matrix.md)

We can manipulate the given linear system one of three ways:
1. Multiply one of equations by a non-zero scalar
2. Interchange two equations
3. Add a multiple of one equation to another

- in 2x2, goal is to have 1 on diagonal, 0 bottom left to isolate $x_2$
- Gaussian elimination, make 0s under 1

[![Image from Gyazo](https://i.gyazo.com/d11b9cd76d1d4287736780cfcc0a34ac.png)](https://gyazo.com/d11b9cd76d1d4287736780cfcc0a34ac)
- If a column has no appropriate 1 upon finding a solution, then it is a parameter
- After isolating one, you slowly go up the chain and substitute and convert into a line

[![Image from Gyazo](https://i.gyazo.com/2358bb2cf6b447cf6a02982676f80737.png)](https://gyazo.com/2358bb2cf6b447cf6a02982676f80737)
- For a specific one, just set t equal to something and prove the point
___

# Backlinks
```dataview
list from [System of linear equations](out/system-of-linear-equations.md) AND !outgoing([System of linear equations](out/system-of-linear-equations.md))
```
___
References:

Created:: 2022-01-19 18:03
