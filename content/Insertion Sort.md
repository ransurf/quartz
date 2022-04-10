---
aliases:
---
Status:
Tags: #archivedCards/cmpt125/algorithms
Links: [[Sorting Algorithms]]
___

# Insertion Sort

## Principles
?
- Good for small n's
- 
- First elem considered sorted

Big O for best, average, worst
?

- For each element, moves when it is smaller than previous index
- Average and worst running time $O(N^2)$
	- Possible for all elements to traverse all the way across
- Best if sorted, no swaps, so O(N) as it still needs to iterate through
<!--SR:!2021-12-17,2,172-->

###
## Question

###### 2018-5
[8 points] How manyswapswill Insertion Sort performon the input [9, 6, 2, 1, 4]
?
ANSWER: 8 swaps
Insert 9: 0 swaps. Result [9, 6, 2, 1, 4]
Insert 6: 1 swap: (6,9). Result [6, 9, 2, 1, 4]
Insert 2: 2 swaps: (2,9), (2,6). Result [2, 6, 9, 1, 4]
Insert 1: 3 swaps: (1,9) (1,6), (1,2). Result [1, 2, 6, 9, 4]
Insert 4: 2 swaps: (4,9), (4,6). Result [1, 2, 4, 6, 9]
<!--SR:!2021-12-16,2,170-->

## Implementation
 void insertionSort(int arr[], int n)
?
```c
{
    int i, key, j;
    for (i = 1; i < n; i++) {
        key = arr[i];
        j = i - 1;
 
        /* Move elements of arr[0..i-1], that are
          greater than key, to one position ahead
          of their current position */
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
```
___
<!--SR:!2021-12-17,2,172-->

# Backlinks
```dataview
list from [[Insertion Sort]] AND !outgoing([[Insertion Sort]])
```
___
References:

Created:: 2021-10-18 16:17
