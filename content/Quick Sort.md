---
aliases:
---
Status:
Tags: #archivedCards/cmpt125/algorithms
Links: [[Sorting Algorithms]]
___

# Quick Sort

## Principles
- It is very efficient for arrays sets that are already substantially sorted

Choosing pivot
?
- way 1: pick first/last
- way 2: largest of 1st 2
- first, mid, last
	- sort, pick median
	- still o(1) and reduces worst case :DDD

Parts
- Pivot
	- Selec element to be pivot
- Partitioning
	- Swap elements such taht elements < pivot are in one partition, elements > pivot are in other

Process
?
- Given an array
	- Choose an element, call it pivot
	- Two pointers, index 1 and n-1
	- Swaps elements at 2 pointers if both pointers are stopped
		- Left stops if elem > pointer
		- Right stops if elem \< pointer
	- As a result:
		1. All elements < pivot are to the left of pivot
		1. All elements >= pivot are to the right of pivot
	- Swap pivot with the rightmost element smaller than pivot
	- Recursively sort to left of pivot
	- Recursively sort to right of pivot
<!--SR:!2021-12-16,2,150-->

Big O composition for good pivots
?
[![Image from Gyazo|400](https://i.gyazo.com/3e146de24a5e0ceeb9b26cdb7f4fd830.png)](https://gyazo.com/3e146de24a5e0ceeb9b26cdb7f4fd830)
   
Parameters of qsort;; qsort(ar3, LENGTH, sizeof(int), cmp_ints);
<!--SR:!2021-12-16,1,130-->

- [[Quick Sort without recursion]]
### Big O Notation
Best case
?
- nlogn
	- has to divide $log_2n$ times before result is 1
		- we partition $O(log_2n)$ times
	- each partition causes up to n-1 comparisons

Worst case
?
- Pivot is largest/smallest
- At most n-1 comparisons
- Partition n-1 times, results in O($n^2$)
### Improvements
Improvement 1
?
- Pivot selection using median-of-3 strat

Improvement 2
?
- Stop using qs when size smal (n<10)
- use insertion instead

Improvement 3
?
- Quick sort calls itself twice
	- Second call:
		- Call done as last operation/tail recursion
		- Replace tail recursion with loop

Improvement 4
?
- First call: call quick sort recursively using smaller partition
### Types of partition and pivots

#### Lomuto partition scheme
- Iterate through array, < pivot get moved while > pivot stay
[![Image from Gyazo](https://i.gyazo.com/a8fbb291088f540f00e656438f8c51b2.png)](https://gyazo.com/a8fbb291088f540f00e656438f8c51b2)

#### Hoare scheme
Hoares
?
```c
int partition(int A[], int l, int h) {

  int pivot = A[l]; //first elem
  int i = l; //set pointers
  int j = h;

  while (i<j) {

    do {
      i++;
    } while (A[i] <= pivot);

    do {
      j--;
    } while (A[j] > pivot);

    if (i<j)
      swap(&A[i], &A[j]);
  }

  swap(&A[l], &A[j]);
  return j;
}

void quickSort(int A[], int l, int h) {
  if (l<h) {
    int j = partition(A, l, h);
    quickSort(A, l, j);
    quickSort(A, j+1, h);
  }
}
```
<!--SR:!2021-12-16,2,150-->
[![Image from Gyazo](https://i.gyazo.com/f81ce39a0eaefbd6be55c89872170ac6.png)](https://gyazo.com/f81ce39a0eaefbd6be55c89872170ac6)

### Time Complexity
Worst case cause and O()
?
- T(n) = O(n) +O(1) + T(n-2)
- Then T(n) = n+(n-2) + (n-4) + (n-6) + … + 2
- = O($n^2$)
- ![Image](https://www.baeldung.com/wp-content/ql-cache/quicklatex.com-45c6fbe2df9decc9f9d864f9f4cac20d_l3.svg)
- caused when pivot is largest element, or when all elems are same
<!--SR:!2021-12-16,1,130-->

Best case
?
- O(nlogn)

Average case
?
O(nlogn)
### Space Complexity
- 

## Examples
What is the sorting process of

Input = [7,1,8,4,10,6,12,3], pivot = 7
?
[![Image from Gyazo](https://i.gyazo.com/f3f132226271e2c88eef1aa4cb5f26c7.png)](https://gyazo.com/f3f132226271e2c88eef1aa4cb5f26c7)
<!--SR:!2021-12-16,2,150-->

Choosing pivot
?
- One that splits array into two equal halves
<!--SR:!2021-12-16,2,170-->

## Code Implementation
___

# Backlinks
```dataview
list from [[Quick Sort]] AND !outgoing([[Quick Sort]])
```
___
References:

Created:: 2021-10-20 14:36
