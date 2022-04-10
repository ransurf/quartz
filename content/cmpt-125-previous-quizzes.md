---
title: CMPT 125 Previous Quizzes
aliases:
---
2Status: 
Tags: #archivedCards/cmpt125/pointers
Links: [CMPT 125 Studying](out/cmpt-125-studying.md)
___

# CMPT 125 Previous Quizzes

## Fall 2020

### Q1

1- Value of x and y, where are ptr and ptr2 pointing?
```
int main(){
	int x = 1;
	int y = 2;
	int* ptr1 = &x;
	int* ptr2 = &y;  *ptr2 = 3;
	ptr2 = ptr1;
	*ptr2 = 4;
	return0;
}
```
?
x = 4, y = 3, both point to x

2- Result of
[![Image from Gyazo](https://i.gyazo.com/342b56ad48b58e0fb6ffdeb6d3db631d.png)](https://gyazo.com/342b56ad48b58e0fb6ffdeb6d3db631d)
?
"20, 30"

### Q2

___

# Backlinks

```dataview
list from [CMPT 125 Previous Quizzes](out/cmpt-125-previous-quizzes.md) AND !outgoing([CMPT 125 Previous Quizzes](out/cmpt-125-previous-quizzes.md))
```
___
References:

Created:: 2021-10-24 13:58
