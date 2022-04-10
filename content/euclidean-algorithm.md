---
title: Euclidean Algorithm
aliases:
---
Status:
Tags:
Links: [Greatest Common Divisor](out/greatest-common-divisor.md)
___

# Euclidean Algorithm

## Principles

### Lemma
Let a = bq + r, where a, b, q, and r are integers. Then gcd(a,b) = gcd(b,r)
?
- Let d be a common divisor of a and b. Then d also divides r = a – bq.
- Thus, d is a common divisor of b and r. Now, let d be a common divisor of b and r.
- Then d also divides a = bq + r.
- Therefore the pairs a,b and b,r have the same common divisors.
- Hence, gcd(a,b) = gcd(b,r).

### Algorithm
?
[![Image from Gyazo](https://i.gyazo.com/1d6f76fe2664b4c316808d5d76edd199.png)](https://gyazo.com/1d6f76fe2664b4c316808d5d76edd199)

## Examples
Find d = gcd(821,123) and integers u and v such that d = 821u + 123v
?
- Right hand side
- Start with last gcd equality, isolate it
	- ex) 40 = 3(13) + 1 becomes 1 = 40 - 3(13)
- Substitute the 2nd last gcd equality by isolating the remainder
	- ex) 40 = 3 x 13 becomes 40 - 3  x 13
- Combine coefficients but don't mix in remainders related to gcd
- Ending coefficients are 
- [![Image from Gyazo](https://i.gyazo.com/c23225549076be3ee07f38099782d76a.png)](https://gyazo.com/c23225549076be3ee07f38099782d76a)
- From 2nd->3rd line, (13)(2) is calculated and the lone 40 is added on top

___

# Backlinks
```dataview
list from [Euclidean Algorithm](out/euclidean-algorithm.md) AND !outgoing([Euclidean Algorithm](out/euclidean-algorithm.md))
```
___
References:

Created:: 2021-11-25 16:56
