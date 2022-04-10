---
title: Combinations with repetitions
aliases:
---
Status:
Tags: #archivedCards/macm101/combinatorics 
Links: [Combinations](out/combinations.md)
___

# Combinations with repetitions
There are C(n + r - 1,n - 1) r-combinations from a set with n elements when repetitions of elements are allowed.

## Examples
How many ways are there to select four pieces of fruit from a bowl containing apples, oranges, and pears if the order in which the pieces are selected does not matter, only the type of fruit and not the individual piece matter, and there are at least four pieces of each type of fruit in the bowl?
?
[![Image from Gyazo](https://i.gyazo.com/0e3ae70d9a144232fe40844ddf8275b3.png)](https://gyazo.com/0e3ae70d9a144232fe40844ddf8275b3)
<!--SR:!2021-12-12,9,181-->

How many solutions does the equation x + y + z = 11 have, where x, y, and z are nonnegative integers?
?
- Stars and bars problem
- Bars act as dividers for the numbers?
- Can also be C(13,11) 
[![Image from Gyazo](https://i.gyazo.com/55907ac80f566cecccf16603e225efc7.png)](https://gyazo.com/55907ac80f566cecccf16603e225efc7)
<!--SR:!2021-12-18,20,230-->

###### Coins

Toss 8 coins, how many outcomes have exactly 3 heads?
?
- Select 3 pos out of 8 for heads, rest tails
- Every solution of a 3-elem subset of 8-elem set
- There are C(8,3) such subsets
<!--SR:!2021-12-19,21,250-->

Toss 8 coins, how many outcomes have at least 3 heads?
?
- Sol'n contains may contain 3,4,5... heads
- Rule of sum, total is sum of ^
- Trick:
	- Total # of outcomes is $2^8$
	- Not interested are 0,1,2 heads
		- # outcomes we are interested in  = $2^8$ - not interested outcomes
<!--SR:!2021-12-22,24,250-->

###### Ticket
100 tickets, numbered 1,2,3,…, 100, are sold to 100 different people for a drawing. Four different prizes are awarded, including a grand prize (a trip to Tahiti). How many ways are there to award prizes if 19 and 47 both win prizes
?
- Choose one prize for 19, C(4,1)
- Choose one prize for 47, C(3,1)
-  Choose 2 winners for the remaining prizes, P(98,2)
<!--SR:!2021-12-16,12,230-->


___

# Backlinks
```dataview
list from [Combinations with repetitions](out/combinations-with-repetitions.md) AND !outgoing([Combinations with repetitions](out/combinations-with-repetitions.md))
```
___
References:

Created:: 2021-11-08 08:50
