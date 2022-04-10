---
title: Greatest Common Divisor
aliases:
---
Status:
Tags: #archivedCards/macm101/numbertheory
Links: [Division](out/division.md)
___

# Greatest Common Divisor

## Principles
- Denoted by `gcd(a,b)`

For integers a and b, a positive integer c is said to be a common divisor of a and b if
?
- c | a and c | b
- For any common divisor d of a and b, we have d | c
<!--SR:!2021-12-11,2,150-->

Prove greatest comon divisor always exists, For any positive integers a and b, there is a unique positive integer c such that c is the greatest common divisor of a and b
?
- Set notation is multiples of all divisors of a,b
[![Image from Gyazo](https://i.gyazo.com/879f761e54d69e944ba334791dc4cbd9.png)](https://gyazo.com/879f761e54d69e944ba334791dc4cbd9)
<!--SR:!2021-12-10,1,130-->

- Finally, if c and d are greatest common divisors, then c | d and d | c. Thus c = d.

### Theorem
Proof: If a, b are integers and d is their greatest common divisor, then there are integers u, v such that d = au + bv.
?
- Keep using previous definitions to climb back to the top
[![Image from Gyazo](https://i.gyazo.com/1f1f88473278820e4370fc814fa57b03.png)](https://gyazo.com/1f1f88473278820e4370fc814fa57b03)
<!--SR:!2021-12-10,1,130-->

## Examples
Greatest common divisor of 42 and 70?
?
[![Image from Gyazo](https://i.gyazo.com/6e10338c661c8000e0955b2fc7c90ad8.png)](https://gyazo.com/6e10338c661c8000e0955b2fc7c90ad8)
<!--SR:!2021-12-11,5,190-->

#### Euclidean Algorithm
- [Euclidean Algorithm](out/euclidean-algorithm.md)
Find greatest common divisor of 821 and 123
?
- Continue using division algorithm to find a smaller comparison for gcd
[![Image from Gyazo](https://i.gyazo.com/31a5a13c53d255c2cda19c4663518ff1.png)](https://gyazo.com/31a5a13c53d255c2cda19c4663518ff1)
___
<!--SR:!2021-12-11,2,150-->

# Backlinks
```dataview
list from [Greatest Common Divisor](out/greatest-common-divisor.md) AND !outgoing([Greatest Common Divisor](out/greatest-common-divisor.md))
```
___
References:

Created:: 2021-11-25 16:32
