---
title: CMPT 125 Big O Notation Practice Problems
aliases:
---
Status: 
Tags: #archivedCards/cmpt125/bigo
Links: [CMPT 125 Practice Problems](out/cmpt-125-practice-problems.md)
___

# CMPT 125 Big O Notation Practice Problems

> [Piazza](https://piazza.com/class/kt82u06t98j7fd?cid=67)

## Questions

1- Let f(n)=n2+10log2(n). Use the formal definition of big-O notation to prove that f(n)=O(n2).  
  

###### 2

[![Image from Gyazo](https://i.gyazo.com/975664b981355e686ee3ea24be024e11.png)](https://gyazo.com/975664b981355e686ee3ea24be024e11)
?
1) Let C=11
2) We show that f(n)≤C⋅$n^4$ for all n>2.
3) Indeed, f(n)=$n^4$+$10log^4(n)$≤$n^4$+$10n^4$=$11n^2$=$Cn^4$. [Here we used the fact that log(n)<n for all n<1, let's say it's log base 2.]
4) We showed that f(n)≤$Cn^4$, therefore f=O($n^4$).
  
<!--SR:!2021-10-29,4,274-->

###### 3

Let f(n)=$n^2$+10⋅n⋅log4(n). Use the formal definition of big-O notation to prove that f(n)=O($n^2$).  
  [hint: use the fact that (log2(n))4`<`n for all n>3]  
? 
1) Let C=11
2) We show that f(n)≤C⋅n⋅$(log2(n))^4$ for all n>3.
3) Indeed, f(n)=n2+10n⋅(log2(n))4≤n2+10n⋅n=11n2=Cn2. [Here we used the fact that (log2(n))4<n for all n<1.]
4) We showed that f(n)≤Cn2, therefore f=O(n4).
  
4- Let f(n)=n2. Prove that it is **not** true that f=O(n). In order to do it you need to show that for every C>0 you try the definition of big-O will not work. That is, for any C you try if n is large enough then f(n)>cn.  
  
  
5- Let f(n)=12+22+32+⋯+n2.  
  Prove that f(n)=O(n3).  
  
  
6- Let f(n)=1∗2+2∗3+3∗4+…(n−1)∗n.  
  Prove that f(n)=O(n3).  
?
it is not true that you can ignore all terms other that the last one.
The solution is the following: In the formula f(n) there are total of n/2 terms, each is at most n2. Therefore f(n)≤(n/2)⋅n2<n3.
  
  
7- Let f(n)=2+4+6+8+⋯+n. (assume that n is even)  
  Prove that f(n)=O(n2).  
?
The sum in the formula for  f(n) has at most n terms, and each of them is at most n. Therefore, f(n)≤n⋅n=n2.
  
  
8- Let f(n)=1+2+4+8+16+32+⋯+n. (assume that n is a power of 2)  
  Prove that f(n)=2n−1. Conclude that f(n)=O(n).  
?
Let k=log2(n). Then f(n)=1+2+4+8+...2k. Using the sum of geometric series formula we have 1+2+22+23+…2k=2k+1−12−1=2k+1−1=2n−1.
  
9- Let f(n)=1^3+2^3+3^3+⋯+n3.  
  Prove that f(n)=O(n4).  
  
10- Suppose that f=O(g) and g=O(h). Prove formally that f=O(h).  
?
[![Image from Gyazo|1000](https://i.gyazo.com/d91a8d36d6ee6fdaa7963c78a1875be3.png)](https://gyazo.com/d91a8d36d6ee6fdaa7963c78a1875be3)
  
  
11- Suppose that f=O(h) and g=O(h). Prove formally that f+g=O(h).  
?
[![Image from Gyazo|1000](https://i.gyazo.com/b63d0987556cc49e4f2a674123bb43db.png)](https://gyazo.com/b63d0987556cc49e4f2a674123bb43db)

12- Let T(n) be given using the recursive formula: T(n)=T(n/2)+1, T(1)=1.  
  Prove that T(n)=O(log(n)).  
?
- T(n)=T(n/2)+1 - by the assumption
- If n>1 let's apply the recursive formula on T(n/2). We get T(n/2)=T(n/4)+1 
- Therefore T(n)=T(n/4)+2
- If we apply it again, we'll get T(n)=T(n/8)+3, and then T(n)=T(n/8)+4.
- More generally, after k applications of the recursion, we'll have T(n)=T(n/$2^k$)+k.
- We will reach the stopping condition of the recursion when n/2k≤1. This happens for k=log2(n).
- Then, we'll have T(n)=T(n/2k)+k=T(1)+log2(n)=1+log2(n)=O(log(n))


13- Let T(n) be given using the recursive formula: T(n)=T(n−1)+n, T(1)=1. Prove that T(n)=O(n^2).  
?
T(n) = T(n-1)+n
= T(n-2) + n-1 + n
= T(n-3) + n-2 + n-1 + n
= T(n-4) + n-3 + n-2 + n-1 + n
...
= n + n-1 + n-2 + n-3 ... 3 + 2 + 1
= n(n+1)/2 = O(n^2)
<!--SR:!2021-10-29,4,280-->

   
14- Let T(n) be given using the recursive formula: T(n)=T(n/2)+n, T(1)=1.  
  Prove that T(n)=O(n).  
?
- Then T(n)=n+T(n/2)
- =n+(n/2)+T(n/4)
- =n+(n/2)+(n/4)+T(n/8)
- =n+(n/2)+(n/4)+(n/8)+T(n/16)⋯
- =
- =n+n/2+n/4+n/8+...+4+2+1=n+1 = O(n)
<!--SR:!2021-10-29,4,278-->


15- Let T(n) be given using the recursive formula: T(n)=2⋅T(n/2)+n, T(1)=1.  
  Prove that T(n)=O(nlog(n)).  
?
T(n) = 2T(n/2) + n
= 2(2T(n/$2^2$) + n/2) + n
= $2^2$T(n/$2^2$) + 2n
= $2^2$(2T(n/$2^3$) + n/4) + 2n
= $2^3$T(n/$2^3$) + 3n
...
= $2^k$T(n/$2^k$) + kn
Assume T(n/$2^k$) = T(1)
n/$2^k$ = 1
n = $2^k$
k = logn
T(n) = $2^k$T(1) + kn
T(n) = nx1+nlogn
O(nlogn)

16- Let T(n) be given using the recursive formula: T(n)=5⋅T(n−1)+1, T(1)=1.  
  Prove that T(n)=O(5n).  
T(n) = 5T

17- Let T(n) be given using the recursive formula: T(n)=T(n/3)+T(2n/3)+n, T(1)=1. Prove that T(n)=O(nlog(n)).  
?

18- Let T(n) be given using the recursive formula: T(n)=T(n/3)+T(2n/3), T(1)=1.  
  Prove that T(n)=O(n).

T(n) = T(n/3) + T(2n/3) = T(n/9) + T(2n/9) 

19- Consider the following function.  
```
int f1 (int n) {
  int sum = 0, i;
  for (i=0; i<n; i++)
    sum += i;
  return sum;
}
```
1. Express in Big O
2. Write the equivalent O(1) function
?
Stops when k>=n
Assume k>=n
k=n
O(n)
<!--SR:!2021-12-24,9,260-->

20- Consider the following function.
```
int f2 (int n) {
  int sum = 0, i;
  for (i=1; i<n; i=i*2)
    sum += i;
  return sum;
}
```
Explain in words the functionality of $f2$. 
?
Returns the series of 1 + $2^1$ + $2^2$ + ... + $2^n-1$ + $2^n$
<!--SR:!2021-12-23,8,254-->


21- f3 gets an array of length n and sets a[i]=$i^2$ for all i
```
void f3 (int* a, int n) {
  for (int i=0; i<n; i++)
    a[i]=i*i;
}
```
Big-O notation.  
Write a function that has the same functionality as f3, runs in O(n) time, but uses only addition, and no multiplication
?
i = 1, 2, 3, ... k
Assume i >= n
k = n
O(n)
<!--SR:!2021-10-28,4,270-->

22- 
```
int f4 (int n) {
  int sum = 0, i, j;
  for (i=0; i<n; i++)
    for (j=1; j<i; j=j*2)
      sum += 1;
  return sum;
}
```
Prove O(nlogn)
?
Outer loop n iterations (0, 1, 2, 3, ... n-1)
Inner loop logn iterations. For every i, there is at most log(i) <= log(n)
<!--SR:!2021-12-22,7,250-->

23- Prove O(n)
```
int f5 (int n) {
  int sum = 0, i, j;
  for (i=1; i<n; i=i*2)
    for (j=1; j<i; j++)
      sum += 1;
  return sum;
}
```
?
For the outer loop we have i=1,2,4,8,16,32...n
For each i we have i iterations of the inner loop.
Therefore, the total running time is 1+2+4+8+...+n<2n
<!--SR:!2021-10-29,4,280-->


___

# Backlinks

```dataview
list from [CMPT 125 Big O Notation Practice Problems](out/cmpt-125-big-o-notation-practice-problems.md) AND !outgoing([CMPT 125 Big O Notation Practice Problems](out/cmpt-125-big-o-notation-practice-problems.md))
```
___
References:

Created:: 2021-10-22 15:33
