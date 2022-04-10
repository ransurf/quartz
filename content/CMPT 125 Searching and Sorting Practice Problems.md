---
aliases:
---
Status: 
Tags: 
Links: [[
___

# CMPT 125 Searching and Sorting Practice Problems

## [Searching and Sorting](https://piazza.com/class/kt82u06t98j7fd?cid=103)

## Problems

1. How many **_comparisons_** and will _Binary Search_ make on input A = [1,2,3,4,5,6,7] when searching for 5?
?
- Compare 5 to 4, go to [5,6,7]
- Compare 5 to 6, go to [5]
- Compare 5 to 5, found elem
    
2. How many **_comparisons_** and how many **swaps** will _SelectionSort_ perform on the array A = [3, 5, 1, 8, 4]? Explain your answer. Write some intermediate steps of the algorithm when necessary.  
?
- Compare 3,5 3,1 1,8 1,4 1 swap (3,1), A = 15384
- Compare 5,3 3,8 3,4 1 swap (3,5), A = 13584
- Compare 5,9 5,4 1 swap (5,4), A = 13485
- Compare 8,5 1 stap (8,5), A = 13458
- 10 comparisons, 4 swaps
        
3. How many **swaps** will _InsertionSort_ perform on the array A = [3, 5, 1, 8, 4]? Explain your answer. Write some intermediate steps of the algorithm when necessary.  
?
- Start at 5, no swap
- Start at 1, swap (5,1), swap (3,1), two swap

4. Consider the _Quicksort_ algorithm that chooses as a pivot the _first_ element of the array. How many **swaps** will it perform on the array A = [6,1,2,3,4,5]? Explain your answer. Write some intermediate steps of the algorithm when necessary.  
      
    
5. Consider the _Quicksort_ algorithm that chooses as a pivot the _last_ element of the array. How many **swaps** will it perform on the array A = [6,1,2,3,4,5]? Explain your answer. Write some intermediate steps of the algorithm when necessary.  
      
    
6. Consider the _MergeSort_ algorithm (with linear time merging we saw in class). How many **_comparisons_** will it perform on the array A = [5,4,3,2,1,4,7,8]? Explain your answer. Write some intermediate steps of the algorithm when necessary.  
      
    
7. Give an example of an array of length n on which _InsertionSort_ makes exactly 1 swap in each iteration of the outer loop.  
      
    
8. Give an example of an array of length 6 on which _InsertionSort_ makes a total of 15 swaps.  
      
    
9. Prove that on any array of length 6 _InsertionSort_ makes at most 15 swaps.  
      
    
10. What is the running time of _InsertionSort_ on a sorted array?
___

# Backlinks

```dataview
list from [[CMPT 125 Searching and Sorting Practice Problems]] AND !outgoing([[CMPT 125 Searching and Sorting Practice Problems]])
```
___
References:

Created:: 2021-10-24 12:10
