---
title: Priority Queue
aliases:
---
Status:
Tags: #cards/cmpt225/dataStructures/adt
Links: [Queue](out/queue.md)
___

# Priority Queue

## Principles
?
- Elements in priority queue are queued in a sorted FIFO fashion using a priority value
- Priority value:
	- Numerical/other sortable value
	- Assigned to element or is attribute of an element
- Dequeue() means we get elem with next priority

### Operations
?
`isEmpty()`
`enqueue()`
`dequeue()`
`peek()`
`getElementCount()`
`dequeueAll()`

### Implementation
Underlying data structure (CDT)
?
- Array
	- Unsorted
	- Sorted
- Linked List
	- Un/Sorted
- BST

### Time Efficiency
Enqueue/Dequeue of unsorted array
?
- Enequeue is O(1), just add to list
- Dequeue is O(n), search through entire array

Enqueue/Dequeue of sorted array
?
- Enequeue is O(n), could end up at end
- Dequeue is O(1) if next item is at end of array
	- O(n) if not since it will have to resize/shift

Unsorted SHSL list insertion
?
- @ Front will be O(1)
- O(n), go to end

Sorted SHSL list insertion
?
- O(n) as will have to find right pos
- O(1) as it will be head

BST insertion
?
- O($log_2n$)

Min binary heap insertion
?
- enqueue() will be O($log_2n$)
- dequeue() will be O(1) since its first element

___
References:

Created:: 2022-03-14 05:56
