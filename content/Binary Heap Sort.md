Status: 
Tags: 
Links: [[Binary Heap]]
___

# Binary Heap Sort
## Principles
To sort an array of n elements
?
- Interpret array as a binary tree in contiguous storage
	- Always complete
	- But may not be heap
- Convert binary tree (array) into binary heap
	- heapify!
- Sort binary heap

### Algorithm

Phase 1
?
- Let index be index of last parent node in binary tree
- while index >= 0
	- reHeapDown(index)
	- index--

Phase 2
?
`heap` is unsorted section of array
1. set counter `unsorted` to n
	- `unsorted` = size of binary heap
1. store last element of heap into temp storage `lastElement`
2. move root to last position in binary heap
3. decrease counter `unsorted` to exclude the last entry from further sorting (becomes first element in sorted section of array)
4. Insert last element into root (position now available)
5. reHeapDown(indexOfRoot) between positions 0 and unsorted - 1
6. Repeat steps 2 to 6 until unsorted is 1

### Time Complexity

Worst case
?
- Phase 1is O(n)
	- Compare parents, for each parent compare children
- Phase 2 is O($nlog_2n$)
	- requires `reHeapDown` which is O($nlog_2n$)x
- Worst case total is O($nlog_2n$)

### Space Complexity
?
- O(1) in place
- If recursive, O($nlog_2n$) for stack frame


___
References:

Created:: 2022-03-17 22:15
