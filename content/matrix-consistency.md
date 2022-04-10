---
title: Matrix Consistency
---
Status: 
Tags: #cards/math232/unit2 
Links: [Matrix Rank](out/matrix-rank.md)
___
# Matrix Consistency
## Principles
- Linear system is consistent iff ;; the rank of the [Coefficient Matrix](out/coefficient-matrix.md) is equal to the rank of the augmented matrix
<!--SR:!2022-02-12,1,130-->
- num pivots (1's) = num of variables

### Inconsistency
- have [ 0 0 0 0 | c ] since c could then be scaled into 1 and that would be a pivot
	- Then would fail the test above when comparing ranks of augmented and coefficient matrix

## Examples
[![Image from Gyazo](https://i.gyazo.com/a54b05bc0b6ae5443819548cf5c40ec4.png)](https://gyazo.com/a54b05bc0b6ae5443819548cf5c40ec4)
___
# Backlinks
```dataview
list from [Matrix Consistency](out/matrix-consistency.md) AND !outgoing([Matrix Consistency](out/matrix-consistency.md))
```
___
References:

Created:: 2022-01-22 13:40
