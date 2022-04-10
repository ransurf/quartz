---
aliases:
---
Status: 
Tags: #cards/cmpt225/dataStructures 
Links: [[Abstract Data Type]]
___

# Queue
- [[Priority Queue]]

Queue
?
- Front, back
- Ordered collection
- `enqueue(item)` add item to queue
- `dequeue()` remove item from queue
- `peek()` Check elem at front of queue
- `isEmpty()` checks if queue is queue
- First in first out (FIFO)
	- ex) Waitlist, line at store
<!--SR:!2022-03-13,2,150-->

- Array to hold elems
- Two pointers, one for head one for tail
- Access to others not allowed
- Not a general purpose data collection

Check if empty ;; if front == back
<!--SR:!2022-03-13,2,150-->
Check if full ;; if back pos = elemCount
<!--SR:!2022-03-12,1,130-->

enqueue()
elems[back++] = 10
back = back % capacity;

Circular, if it goes above size then it goes back to 0

### Use Cases
- Pipeline architecture
	- A program can use queue to perform a lot of request using queue acting as a buffer
	- Ex. Print buffer, keyboard buffer
- Server requests
- Database requests
- CPU scheduler
### Big O Notation
- array-based O(1)
- link-based P(1) but dequeueAll() is O(n)
- list adt-based uncertain
___

# Backlinks

```dataview
list from [[Queue]] AND !outgoing([[Queue]])
```
___
References:

Created:: 2021-10-27 14:56
