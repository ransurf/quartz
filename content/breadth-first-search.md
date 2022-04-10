---
title: Breadth First Search
aliases:
---
Status:
Tags:
Links: [Binary Tree Traversal](out/binary-tree-traversal.md)
___

# Breadth First Search
`16-48`
- Elementsa re visited in a FIFO system, all nodes are visited before next
## Using Stack
### Implementation
```
PreOrder(root):
	s = create stack of nodes
	s.push(root)
	While s is not empty:
		node = s.pop()
		printf(node->value)
		if (node->right != NULL)
			s.push(node->right)
		if (node->left != NULL)
			s.push(node->left)
```
### Traversal
On graph:
[![Image from Gyazo](https://i.gyazo.com/7ddec7dcca20bdc2c9ce9d1273b14715.png)](https://gyazo.com/7ddec7dcca20bdc2c9ce9d1273b14715)
[![Image from Gyazo](https://i.gyazo.com/8193a891339e2364048381e1765c6bce.png)](https://gyazo.com/8193a891339e2364048381e1765c6bce)


## Using Queue
- Prints layer by layer, as the child nodes get sent to the back

### Implementation
```
BreadthFirstSearch(root):
	q = create queue of nodes
	q.enqueue(root)
	while q is not empty:
		node = q.dequeue()
		printf(node->value)
		if (node->left != NULL)
			q.enqueue(node->left)
		if (node->right != NULL)
			 q.enqueue(node->right)
```

### Traversal
On graph:
[![Image from Gyazo](https://i.gyazo.com/7ddec7dcca20bdc2c9ce9d1273b14715.png)](https://gyazo.com/7ddec7dcca20bdc2c9ce9d1273b14715)
?
[![Image from Gyazo](https://i.gyazo.com/d660253be946a4c4910fe1cc45d91ad9.png)](https://gyazo.com/d660253be946a4c4910fe1cc45d91ad9)
___

# Backlinks
```dataview
list from [Breadth First Search](out/breadth-first-search.md) AND !outgoing([Breadth First Search](out/breadth-first-search.md))
```
___
References:

Created:: 2021-11-10 15:02
