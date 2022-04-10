Status: 
Tags: #archivedCards/macm101/numbertheory 
Links: [[Integers]]
___
# Division
- Division
	- a | b implies a divides b
- [[Greatest Common Divisor]]

Let n and d be positive integers. How many positive integers not exceeding n are divisible by d?
?
- dk is a number divisible by k, have 0 < dk <= n, 0 < k <= n/d, answer is floor(n/d)
<!--SR:!2021-12-10,1,130-->

Properties of divisibility (a,b,c)
?
- if a | b and a | c, then a | (b+c)
- if a | b, then a | bc for all integers c
- if a | b and b | c then a | c
<!--SR:!2021-12-10,1,148-->

Prove that a | b and a | c implies that there are k and m such that b = ak and c = am
?
Then b + c = ak + am = a(k+m), and a divides b + c
<!--SR:!2021-12-10,1,130-->

Prove that a | b and a | c implies that there are a | mb + nc whenever m and n are integers
?
- rule 2 states that a | mb and a | nc
- part 1 implies a | mb + nc
<!--SR:!2021-12-11,2,150-->

If a | b and  b | a, then a = +- b
?
Suppose that a | b and b | a
- Then b = ak and a = bm for some integers k and m
- Therefore a = bm = akm, which is possible only if k,m = +- 1
<!--SR:!2021-12-10,2,130-->

How to find mn when given lcm and gcd
?
ab = lcm(a,b) x gcd(a,b)
<!--SR:!2021-12-10,2,131-->

Finding number of positive divisors for a number
?
multiply each prime number +1
ex) if prime factorization is $2^3(3)$, then # of divs is $2^4(3)^2$ = 144
<!--SR:!2021-12-10,2,131-->

___
# Backlinks
```dataview
list from [[Division]] AND !outgoing([[Division]])
```
___
References:

Created:: 2021-11-25 15:32
