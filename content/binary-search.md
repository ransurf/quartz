---
title: Binary Search
---
Status: 
Tags: 
Links: [Searching a sorted array](out/searching-a-sorted-array.md)
___
# Binary Search
## Principles
- Rounds up on odd lengths
## Big O
T(N) = T(N/2) + O(1)
- T(N/2) since it reruns function on half of array
- If statements are O(1)

Solving
O(1) is some constant, assume c=4
```c
T(N) = T(N/2) + C
= T(N/4) + 2C //T is cut in half again,another c is added, thus 2c
= T(N/8) + 3C

[For i > 0] = T(N/2i) + i*C //knowing the purpose of i
[For i = log2(N)] = T(1) + log2(N)*C ​ //when it stops
= O(log(N)) //simplifcation
```
## Examples
[Binary Search in Replit](https://replit.com/@JohnReyes08/cmpt125-2021-10-18#main.c)

___
# Backlinks
```dataview
list from [Binary Search](out/binary-search.md) AND !outgoing([Binary Search](out/binary-search.md))
```
___
References:

Created:: 2021-10-17 16:31
