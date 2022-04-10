---
title: Matrix
aliases:
---
Status:
Tags: #cards/math232/unit3
Links: [MATH 232 Units](out/math-232-units.md)
___

# Matrix

## Principles
- Element in matrix is called ;; entries
<!--SR:!2022-02-22,11,170-->

Syntax (size, specific element)
?
- Denote size by $A_{mxn}$
- Denote specific element by $[aij]_{mxn}$ or $[aij]$ or $(A)_{ij}$
<!--SR:!2022-02-16,5,134-->

- [Matrix Operations](out/matrix-operations.md)
- [Matrix Vector Multiplication](out/matrix-vector-multiplication.md)

- Matrices can scale, reflect, rotate
- Some matrices are length preserving
- 
### Types
Square matrix
?
- m=n
- when i=j then it is a diagonal entry
<!--SR:!2022-04-10,38,160-->

Diagonal matrix
?
- a square matrix where non-diagonal entries are all 0
<!--SR:!2022-02-18,7,152-->

**Identity Matrix**
?
- when all diagonal entries are 1
- Resembles 1 of matrixes
- multiplicative identity element (nothing happens when we multiply with another matrix)
- Always square
- Diagonal, UT, LT
- Column vectors and row vectors and standard basis vectors for R^n where n is columns
<!--SR:!2022-02-22,11,170-->

Triangular matrix
?
- Upper triangular or lower triangular
	- A is UT if aij = 0 for every i>j
	- A is LT if aij = 0 for every j>ix

- [Standard Matrix](out/standard-matrix.md)
### Decomposition into vectors
?
- Matrix can be turned into a row list of columnar vectors or
	- each column is vector
- a columnar list of row vectors
	- each row is vector
- [![Image from Gyazo](https://i.gyazo.com/0ba5a416132dd46f4778f9d8f5960b00.png)](https://gyazo.com/0ba5a416132dd46f4778f9d8f5960b00)

### Characteristics
- [Matrix Span](out/matrix-span.md)
- [Matrix linear independence](out/matrix-linear-independence.md)
- [Matrix Transpose](out/matrix-transpose.md)
- [Matrix Linearity Properties](out/matrix-linearity-properties.md)
- [Matrix Mapping](out/matrix-mapping.md)
## Examples
___

# Backlinks
```dataview
list from [Matrix](out/matrix.md) AND !outgoing([Matrix](out/matrix.md))
```
___
References:

Created:: 2022-01-25 19:57
