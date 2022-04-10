---
aliases:
---
loadStatus:
Tags: #archivedCards/cmpt125/bigo
Links: [[Big O Notation]]
___

# Big O Notation Calculating Time Complexity

## Principles

### Multiple Inputs
- Attend to all inputs, could be O(ab)

#### Varying Lengths
Array of strings, sorted each string, then sorted array
?
- Let s be length of longest string
- Let a be length of array
- O(s logs) for sorting strings, then O(a) for sorting array
- Happens 

### Recursive Calls
- When multiple calls are made, it will most likely be O($branches^{depth}$)
	- *ex) If 2 recursive calls, then 2 branches*

### General Methodology
- Find out how many times it iterates via series `1 + 2 + ... + N`
- Combine other relevant things
- Profit

## Code Operations
Steps for for loops
?
- find out how the pattern for i
- Assume the stopping condition is met `ex. i>=n`
- Set i to the pattern found
- Isolate k to find n
<!--SR:!2021-12-21,6,250-->

- [[Recurrence Relation]]
Steps for Recursion
?
- Write formula in non-recursion
- Determine stopping condition, when N will become 1
- ex) foo(N/2) will be O(logN)
<!--SR:!2021-10-30,7,252-->

<!--SR:!2021-10-20,1,230-->

Recursive T(N-1) is;; O(n)
<!--SR:!2021-11-04,12,270-->

Recursive T(N/2) is O;; (logN)
<!--SR:!2021-10-31,6,270-->

### Recursion

### For Loops
`for(i=1;i<n;i=i*2)`
?
[![Image from Gyazo](https://i.gyazo.com/00804a8ab32386d979a09fa65567e8c9.png)](https://gyazo.com/00804a8ab32386d979a09fa65567e8c9)
<!--SR:!2021-12-25,10,230-->

`for (i=n; i>=1; i=i/2)`
?
[![Image from Gyazo](https://i.gyazo.com/d8a2dce78662de0cddabf579f2ef1570.png)](https://gyazo.com/d8a2dce78662de0cddabf579f2ef1570)
<!--SR:!2021-10-27,3,265-->

`for (i=0; i*i<n; i++)`
?
- i*i < n is stopping condition, so i*i >= n
- $i^2$ = n
- i = $\sqrt{n}$
<!--SR:!2021-10-29,4,273-->

*Explain the process*
[![Image from Gyazo](https://i.gyazo.com/2db1fc2ff048964757caf3d2771fd630.png)](https://gyazo.com/2db1fc2ff048964757caf3d2771fd630)
?
[![Image from Gyazo](https://i.gyazo.com/56fd3c9004474652d55080b3693bf4cd.png)](https://gyazo.com/56fd3c9004474652d55080b3693bf4cd)
<!--SR:!2021-10-27,3,210-->

___

# Backlinks
```dataview
list from [[Big O Notation Calculating Time Complexity]] AND !outgoing([[Big O Notation Calculating Time Complexity]])
```
___
References:

Created:: 2021-10-19 14:11
