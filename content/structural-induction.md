---
title: Structural Induction
---
Status: 
Tags: #archivedCards/macm101/induction 
Links: [Mathematical Induction](out/mathematical-induction.md)
___
# Structural Induction


- Height of binary tree, h(T)
- Recursive definition:
	- Basis step: Height of a single vertex `r` is 0, h(r) = 0
	- Inductive step: Tree T is built from trees $T_1$, $T_2$ as shown in inductive step, h(T) = 1 + max of $T_1$, $T_2$

Prove [Rooted Tree](out/rooted-tree.md) using mathematical induction
?
- Basis case: Single vertex is binary tree
- [![Image from Gyazo](https://i.gyazo.com/9d7b7271bd00890ebe3e029557dd5c27.png)](https://gyazo.com/9d7b7271bd00890ebe3e029557dd5c27)
<!--SR:!2021-12-15,7,150-->

Proving number of vertices in a binary tree, n(T), satisfied equality n(T) <= $2^{h(T)+1}$ - 1
?
[![Image from Gyazo](https://i.gyazo.com/ae441e17e6417d49e8dbe1ecc973cf1e.png)](https://gyazo.com/ae441e17e6417d49e8dbe1ecc973cf1e)
<!--SR:!2021-12-10,4,130-->

___
# Backlinks
```dataview
list from [Structural Induction](out/structural-induction.md) AND !outgoing([Structural Induction](out/structural-induction.md))
```
___
References:

Created:: 2021-11-04 09:04
