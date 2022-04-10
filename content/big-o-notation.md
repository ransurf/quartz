---
title: Big O Notation
---
Status: 
Tags: #archivedCards/cmpt125/algorithms - [Space Efficiency](out/space-efficiency.md)
Links: [Measuring performance time of algorithms](out/measuring-performance-time-of-algorithms.md)
___
# Big O Notation
## Principles
Helps measure
?
- Time
	- # operations, loop iterations
- space
	- additional memory needed

- [Big O Notation Definition](out/big-o-notation-definition.md)
- [Big O Notation Calculating Time Complexity](out/big-o-notation-calculating-time-complexity.md)
- [Big O Notation Orders of Magnitude](out/big-o-notation-orders-of-magnitude.md)
- [CMPT 125 Big O Notation Practice Problems](out/cmpt-125-big-o-notation-practice-problems.md)

- sequence 1 = s1, sequence 2 = s2
- sequential operations O(s1 + s2)
- Repeated k times? O(ks1)
- For loops? (O(s1 x s2))

- Average case is anything else other than best and worst
## Examples

Geometric summation for 2N;; N+(N/2+N/4+N/8+N/16) <= 2N, total running time, big o
<!--SR:!2021-12-20,7,210-->

### Arithmetic
 Summation would be 2-3N
- Straight forward, based on length of n

 Multiplication would be $n^2$
 - Multiply each digit by each digit
 - based on length of n
 
 Finding factor of 2 primes
 - Runtime would be $10^{n}$ where n=actual digit

## Practice
[Exercises](https://1sfu-my.sharepoint.com/:p:/g/personal/jmr26_sfu_ca/EUnPmjFtauFBvpdj54EiX7UBqzXXkmK7NSIIH4QP-Z0ZDA?e=gP5UEe)
[SO practice problems](https://stackoverflow.com/questions/11094330/determining-the-big-o-runtimes-of-these-different-loops)
[Runtime flashcards](https://quizlet.com/324002059/sorting-algorithms-runtime-flash-cards/)
- Proving big o notation
- Comparing big o runtimes

___
# Backlinks
```dataview
list from [Big O Notation](out/big-o-notation.md) AND !outgoing([Big O Notation](out/big-o-notation.md))
```
___
References:

Created:: 2021-10-06 14:32
