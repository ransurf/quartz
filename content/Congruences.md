---
title: Congruences
aliases: modulo
---
Status:
Tags: #archivedCards/macm101/settheory #archivedCards/macm101/numbertheory
Links: [Discrete Math Relations](out/discrete-math-relations.md) - [Integers](out/integers.md)
___

# Congruences

## Principles
- [Residues](out/residues.md)
- [Linear Congruences](out/linear-congruences.md)

Definition in terms of notation
?
[![Image from Gyazo](https://i.gyazo.com/6c67d0049fe6985c68c5d3f975cce6db.png)](https://gyazo.com/6c67d0049fe6985c68c5d3f975cce6db)
<!--SR:!2021-12-09,2,154-->

Define and prove in terms of euclidean algorithm
?
a ≡ b (mod m) if and only if a = b + km for some integer k
By definition, a ≡ b (mod m) if and only if a – b = km for some integer k. Then a = b + km
<!--SR:!2021-12-08,1,134-->

Integers a and b are congzruent modulo m iff they have same remainder when divided by m.
If a-b = km, b = qm + r, then
?
a = km + b = (k+q)m + r
<!--SR:!2021-12-08,1,134-->

### Uses
- [Caesar Cipher](out/caesar-cipher.md)
- [Psuedorandom Generators](out/psuedorandom-generators.md)

## Theorems
Prove if a ≡ b (mod m) and c ≡ d (mod m), then ac ≡ bd (mod m)
?
[![Image from Gyazo](https://i.gyazo.com/7e17cf8253733b3e7a674d0364497ff9.png)](https://gyazo.com/7e17cf8253733b3e7a674d0364497ff9)
<!--SR:!2021-12-10,1,130-->

## Examples
12 = 5 (mod 7)
12 = 6 (mod 3)
12 = -3 (mod -15)
12 = 0 (mod 12)

Prove congruences are equivalent relations (k,a,b)
?
[![Image from Gyazo](https://i.gyazo.com/17a68ba1839d0dcf3da67f684002f8a3.png)](https://gyazo.com/17a68ba1839d0dcf3da67f684002f8a3)
<!--SR:!2021-12-13,6,190-->

Congruences definition with integers k, a, b
- Example when k is 3
?
[![Image from Gyazo](https://i.gyazo.com/9a96b8c4a1f7bbb7b64a3b248233efd2.png)](https://gyazo.com/9a96b8c4a1f7bbb7b64a3b248233efd2)
- Refer to modulo in coding
<!--SR:!2021-12-09,2,154-->

___<!--SR:!2021-12-18,11,250-->

# Backlinks
```dataview
list from [Congruences](out/congruences.md) AND !outgoing([Congruences](out/congruences.md))
```
___
References:

Created:: 2021-10-26 16:40
