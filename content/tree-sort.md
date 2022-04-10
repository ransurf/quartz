---
title: Tree Sort
---
Status: 
Tags: #cards/cmpt225/dataStructures/adt 
Links: [Sorting Algorithms](out/sorting-algorithms.md)
___

# Tree Sort
## Principles
- Uses sorting property of [AVL](out/self-balancing-binary-search-tree.md) trees
	- Becomes sorted as you convert array into BST
	- In-order traversal to transfer back into array
### Big O Notation
?
Phase 1- Building BST
- Average case: 1 insertion will be O($log_2n$), n insertions will be O($nlog_2n$)
- Worst case: 1 insertion will be O(n), so n insertions will be O($n^2$)
<!--SR:!2022-03-13,2,150-->

Phase 2- Traversing and back into array
- Average case: O($nlog_2n$)

Space efficiency is O(n)

___
References:

Created:: 2022-03-09 19:46