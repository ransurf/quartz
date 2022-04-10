---
title: Least Common Multiple
---
Status: 
Tags: 
Links: [Integers](out/integers.md)
___
# Least Common Multiple
## Principles
- A positive integer c is called a `common multiple` of integers a and b if ;; a | c and b | c

- Number c  is the lcm(a,b) if ;; for any common multiple d we have c | d
## Theorem
Find lcm(231, 455) brute force method
?
- 231 = 3(77) = 3(7)(11)
- 455 = 5(91) = 5(7)(13)
- lcm(231,455) = 3(7)(11)(5)(13)
	- Don't count duplicates, consider highest degree

For any integers a and b, the least common multiple exists where ab = ;; lcm (gcd(a,b))

Find lcm(231,455) using theorem
?
- lcm(a,b) = (ab)/(gcd(a,b))
- Find gcd which is 7
- lcm(a,b) = (231 x 455)/7 = 

___
# Backlinks
```dataview
list from [Least Common Multiple](out/least-common-multiple.md) AND !outgoing([Least Common Multiple](out/least-common-multiple.md))
```
___
References:

Created:: 2021-11-29 20:35
