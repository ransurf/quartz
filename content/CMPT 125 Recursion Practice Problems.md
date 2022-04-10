Status: 
Tags: #archivedCards/cmpt125/recursion
Links: [[CMPT 125 Practice Problems]]
___
# CMPT 125 Recursion Practice Problems
[Piazza](https://piazza.com/class/kt82u06t98j7fd?cid=104)
## Questions
1- "3 2 1", while loop from n to 1

2- 
"1 2 3", while loop from 1 to n+1

3- Prints for n=3?
```
int foo(int n) {
  if (n == 0)
    printf("0 ");
  else {
    printf("%d ", n);
    foo(n-1);
    printf("%d ", n);
  }
}
```
?
"3 2 1 0 1 2 3", yeah

4- Functionality? Prints on 3?
```c
long foo(int n) {
  if (n==0) return 1;
  else return foo(n-1)+foo(n-1);
  }
}
```
?
3, 2 2, 1 1 1 1, 0 0 0 0 0 0 0 0, $2^n$

5- Functionality, n=3?
```c
void foo(int n) {
  if (n == 0)
    printf("*");
  else {
    foo(n-1);
    foo(n-1);
  }
}
```
?
Prints $2^k$ amount of asterisks, n=3 equals `********`

6-
```c
int foo1(int n) {
  if (n <= 1)
    return n*2;
 	
  int half = n/2; // round down if n is odd
  int n1 = foo1(half);
  int n2 = foo1(n-half);
  return (n1+n2);
}
```
?
Returns n*n
```c
void foo1(int n) {
	return n*n;
}
```

7-


___
# Backlinks
```dataview
list from [[CMPT 125 Recursion Practice Problems]] AND !outgoing([[CMPT 125 Recursion Practice Problems]])
```
___
References:

Created:: 2021-10-22 22:08
