---
title: Mathematical Induction
aliases:
---
Status:
Tags:  #archivedCards/macm101/induction
Links: [Discrete Mathematics](out/discrete-mathematics.md)
___

# Mathematical Induction

## Principles
[Well Ordering Principle](out/well-ordering-principle.md)

### Definition
?
To prove a statement that asserts some property P(n) is true for all positive integers n
- if p(k) is true then p(k+1) is true
- Symbolically
	- (P(1) ∧ ∀k (P(k) → P(k + 1))) → ∀n P(n)
<!--SR:!2021-12-10,4,130-->

### Steps
?
- Two steps:
	- Verify base case (usually P(1)) is true
	- Assume n=k, k>=1
		- Rewrite formula in terms of k
	- Rewrite original formula with addition of k+1 case on left side
		- On right side replace n with k+1
	- Inductive step: Show that conditional statement P(k) -> P(k + 1) is true for all positive integers k
		- Replace the solved left part using the base case, them mix like terms to make both sides equal
<!--SR:!2021-12-12,3,150-->

### Proving
?
- P(n) denotes `statement`
	- Prove it is true
- Suppose P(k) is true, that is `statement but any var`
	- Prove P(k+1)
<!--SR:!2021-12-10,7,170-->

## Types
- [Mathematical Summation](out/mathematical-summation.md)
- [Strong Induction](out/strong-induction.md)
- [Structural Induction](out/structural-induction.md)

## Examples
Give a recursive definition of f(n) = $2^n$
?
Basis step: f(0) = 1
Inductive step: f(k + 1) = 2 ⋅ f(k).
<!--SR:!2021-12-10,7,150-->

Factorial induction
?
- f(n) = n!
- Basis step: 0! = 1
- Inductive step: (k + 1)! = k! ⋅ (k + 1)
<!--SR:!2021-12-17,9,150-->

Trimonio can fill square missing a tile
?
- Prove the first case of a 2x2 grid
- For a larger case, place the trimonio so all squares have a covered tile
	- Since last step was proved, it is possible
<!--SR:!2021-12-14,11,170-->


___

# Backlinks
```dataview
list from [Mathematical Induction](out/mathematical-induction.md) AND !outgoing([Mathematical Induction](out/mathematical-induction.md))
```
___
References:

Created:: 2021-10-28 09:56
