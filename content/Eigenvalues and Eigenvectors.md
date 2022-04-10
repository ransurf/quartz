---
aliases:
---
Status:
Tags: #cards/math232/unit6
Links: [[Vectors]]
___

# Eigenvalues and Eigenvectors
- [[Eigenvectors of Linear Mappings]]
## Principles
Eigenvalue and Eigenvector
?
- Special vector of matrix that is mapped by the matrix to a scalar multiple of itself
- [![Image from Gyazo](https://i.gyazo.com/ea0eee5aa73d3aacc63a0e121c958888.png)](https://gyazo.com/ea0eee5aa73d3aacc63a0e121c958888)
- eigenvector should be non-zero
- Each eigenvector of A will lead to an eigenvalue, but each eigenvalue will have infinitely many eigenvectors
<!--SR:!2022-03-26,1,130-->

Characteristic polynomial
?
- C(λ) = det(A-λI)
- Highest degree has coefficient $(-1)^n$

### Dominant Eigenvalue
Dominant eigenvalue
?
- The eigenvalue larger than the rest

Power method for approximating eigenvalues
?
[![Image from Gyazo](https://i.gyazo.com/35fe203e610814528e4bf4bf33d23928.png)](https://gyazo.com/35fe203e610814528e4bf4bf33d23928)
- Choose random vector (do [1,1]) and find right value through eqn
- then keep multiplying matrix with newfound vector until you see a pattern and deduce the eigenvector
- Do matrix multiplication with A and deduced eigenvector, then GCF out the number $c$ to have $c\vec{v}$
	- $c$ is dominant eigenvalue
<!--SR:!2022-03-26,1,130-->

### Algebraic and Geometric Multiplicity
Algebraic multiplicity
?
- alg mult of λ is number of times λ is repeated as a root of the characteristic polynomial
	- Literally just degree of the root
<!--SR:!2022-03-27,2,151-->

Geometric multiplicity
?
- geo mult is dimension of eigenspace of λ
	- The number of vectors in the nullspace basis

Relationship between alg and geo mult
?
- 1 <= geo mult <= alg mult

geo < alg implies that the eigenvalue is ;; deficient

if for all eigenvalues, geo mult = alg mult, then
?
- sums will equal each other which equal n
- if we collect all basis vectors from eigenspaces, we will end up with n vectors in $R^n$
	- linear independent, form as basis for $R^n$
<!--SR:!2022-03-26,1,130-->

A is invertible implies that
?
- λ is not an eigenvalue of A
<!--SR:!2022-03-26,1,130-->

### Finding Eigenvalues of a Matrix A
?
- refer to pg. 350 / 367
- There must be v1,v2 != 0 such that A[v1,v2] = λ[v1,v2]
- Can be turned into linear systems, turn into standard form (=0)
- Only eigenvalue if non-zero solutions provide a non-zero vector v
	- Use [[Matrix Inverse#Invertible Matrix Theorem]] / use determinant to see when determinant = 0
		- ad-bc, find root of polynomial
<!--SR:!2022-03-26,1,130-->

### Finding infinite eigenvectors of eigenmatrix
?
- Find solution space of homogeneous system with coefficient matrix
[![Image from Gyazo](https://i.gyazo.com/d905df8d24e4e68e888cc6a10f29448a.png)](https://gyazo.com/d905df8d24e4e68e888cc6a10f29448a)
- Nullspace of $(A-λ)\vec{v}$
- Only add λ to a and d, then RREF

### Eigenspace
?
[![Image from Gyazo](https://i.gyazo.com/1e4eeeaa2924b5bc0a2488229aacfc50.png)](https://gyazo.com/1e4eeeaa2924b5bc0a2488229aacfc50)
- Minimum 1 dimension
<!--SR:!2022-03-26,1,130-->

## Examples
[![Image from Gyazo](https://i.gyazo.com/438d307468b2bf57e1f8541b4da561a3.png)](https://gyazo.com/438d307468b2bf57e1f8541b4da561a3)
?
[![Image from Gyazo](https://i.gyazo.com/34c82ea80d7d5b4fd24c980d1353403b.png)](https://gyazo.com/34c82ea80d7d5b4fd24c980d1353403b)
<!--SR:!2022-03-26,1,130-->

Find eigenvalues and vectors of the matrix A =
$\begin{bmatrix} 
17 & -15 \\20 & -18 
\end{bmatrix}$
?
[![Image from Gyazo](https://i.gyazo.com/e82c2f4f97e6daadec6db487409ba8ec.png)](https://gyazo.com/e82c2f4f97e6daadec6db487409ba8ec)
___
References:
<!--SR:!2022-03-27,2,150-->

Created:: 2022-03-09 16:25
