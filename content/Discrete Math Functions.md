---
aliases:
---
Status: #🔗
Tags: #archivedCards/macm101/settheory
Links: [[MACM101 Outline]]
___

# Discrete Math Functions

## Principles
Functions definition
?
In a relation R from A to B, for every a ∈ A there is exactly one b ∈ B such that (a,b) ∈ R. (Also mappings, transformations)
- ex) f(a) = b if b is the father of a
- Notation is f: A -> B
<!--SR:!2022-02-03,60,230-->

### Types
One-to-one/injective functions
?
- If and only if f(a) = f(b) implies a = b
- if a ≠ b then f(a) ≠ f(b)
- ∀a ∀b (f(a) = f(b) → a = b)
<!--SR:!2021-12-10,4,194-->

Proving one-to-one/injective
?
- Start with starting function, and slowly isolate a and b
<!--SR:!2021-12-10,1,180-->

Onto/surjective and surjection functions
?
- Function f if and only if for every element b ∈ B there is an element a ∈ A with f(a) = b. A function is called a surjection if it is onto
- ∀b ∃a (f(a) = b)
- Notation: f(x) = x + 1
<!--SR:!2021-12-20,32,270-->

Proving onto/surjective
?
find inverse in term of a and b through f(a) = b
<!--SR:!2021-12-10,3,220-->

One-to-one correspondence/bijection if it is ;; both one-to-one and onto
<!--SR:!2022-01-20,46,234-->

Identity function ;; i$_A$: A -> A where i$_A$(x) = x
<!--SR:!2022-01-10,35,174-->

Permutation ;; bijection from set A to same set A
<!--SR:!2022-01-21,47,234-->

Describing functions
?
- Function table
- f(x) = `mapping`
- range(f) = {0,4,9,...} non-negative ints that are perfect squares
<!--SR:!2021-12-14,7,227-->

Composition
?
- (f o g)(a) = f( g(a) )
	- Do g(a) first, then do f
<!--SR:!2022-01-24,50,235-->

### Characteristics

###### Domain
Describe domain and co-domain using A and B
?
f: A->B
- If f(a) = b
	- b is called the image of a, and a is called the preimage of b
		- we say that f maps A to B
- ex) domain = { Adams, Chou, Goodfriend, Rodriguez, Stevens }
	- codomain = { A, B, C, D, F } range = { A, B, C, F }
<!--SR:!2022-02-06,61,270-->



###### Range
?
range of f is the set of all images of elements of A
- range(f) = { b ∈ B | ∃a ∈ A f(a) = b }
<!--SR:!2022-02-10,66,230-->

###### Restrictions
?
Let f: A → B be a function and C ⊆ A
- The set f(C) = { b ∈ B | b = f(a) for some a ∈ C } is called the image of C
- Notation is f|$_c$
	- ex) f|$_c$: C->B is a restriction of f to C if f|$_c$(a) = f(a) for all a e C
		- Same function, just less elements due to restriction
<!--SR:!2022-02-16,72,250-->

###### Extensions
?1
Let C ⊆ A and f: C → B
- Any function g: A → B such that g(a) = f(a) for all a ∈ C is called an extension of f

## Examples
If f:X→Yand g:Y→Z are functions and g◦f:X→Zis one-to-one, must both fand g be
one-to-one? Prove or give a counterexample.
?
Solution: Consider function f:{a, b, c} → {1,2,3,4}and function g:{1,2,3,4} → {d, e, f }. Let f={(a, 1),(b, 2),(c, 3)}and g={(1, d),(2, e),(3, f ),(4, f)}. Observe that g is not one-to-one
<!--SR:!2021-12-08,3,174-->

Show that the union of two countably infinite sets is also countably infinite.
?
- Let the two countable infinite sets be Aand B. Since both sets are countably infinite, there is a
- sequence Sa=a1,a2,. . .,ai,. . ., (Sb=b1,b2,. . .,bi,. . .,) in which the elements in set A(B) are visited.
- We construct the sequence Sc=a1,b1,a2,b2,. . .,ai,bi,. . . in the which the elements in set C=A∪B
- are visited. Observe that every element c∈Cis visited because coccurs either in Aor B, and every element in Aand Bis visited in the sequence Sc
<!--SR:!2022-01-31,56,267-->

___

# Backlinks
```dataview
list from [[Discrete Math Functions]] AND !outgoing([[Discrete Math Functions]])
```
___
References:

Created:: 2021-10-28 09:06
