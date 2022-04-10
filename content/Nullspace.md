---
aliases: kernel
---
Status:
Tags: #cards/math232/unit3 
Links: [[Linear Mapping]]
___

# Nullspace

## Principles
Nullspace
?
[![Image from Gyazo](https://i.gyazo.com/8cacc8b371863bf8cf220fbec0ef65ef.png)](https://gyazo.com/8cacc8b371863bf8cf220fbec0ef65ef)
- Set of all vectors whose image under L is the zero vector
- Nullspace is subspace
- Solution space of homogeneous equation

As a linear mapping
?
[![Image from Gyazo](https://i.gyazo.com/31869651823773a95aba1180976c7d58.png)](https://gyazo.com/31869651823773a95aba1180976c7d58)

Prove that nullspace is a subspace
?
[![Image from Gyazo](https://i.gyazo.com/00add5e9c4b0e9ac266f7646d4949e73.png)](https://gyazo.com/00add5e9c4b0e9ac266f7646d4949e73)
[![Image from Gyazo](https://i.gyazo.com/1754c4e657b457103ea277a682ab2484.png)](https://gyazo.com/1754c4e657b457103ea277a682ab2484)
<!--SR:!2022-02-17,6,152-->

Dimension of nullspace is
?
- number of free variables
- num columns - rank
<!--SR:!2022-02-21,10,170-->

- [[Four fundamental subspaces]]
## Examples
- Find nullspace of [![Image from Gyazo](https://i.gyazo.com/a4539ebf59136bc2ea86ccd47657711b.png)](https://gyazo.com/a4539ebf59136bc2ea86ccd47657711b)
?
- Create matrix, row reduce, back substitution to find solution set of vectors (x1,x2,x3) where L(x) = 0
- [![Image from Gyazo](https://i.gyazo.com/2b9c3e5e5c33f82ed471c0c835827c20.png)](https://gyazo.com/2b9c3e5e5c33f82ed471c0c835827c20)
- is basis for Null(L)
<!--SR:!2022-03-06,3,132-->

Check if vector x is in nullspace A
?
- If Ax = 0, it is in nullspace
- If it is in the nullspace, then Ax = 0
___
<!--SR:!2022-02-12,1,138-->

# Backlinks
```dataview
list from [[Nullspace]] AND !outgoing([[Nullspace]])
```
___
References:

Created:: 2022-02-01 15:44
