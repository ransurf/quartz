---
title: Binary Tree Traversal
aliases:
---
Status:
Tags:
Links: [Binary Tree](out/rooted-tree.md)
___

# Binary Tree Traversal
[![Image from Gyazo](https://i.gyazo.com/7ddec7dcca20bdc2c9ce9d1273b14715.png)](https://gyazo.com/7ddec7dcca20bdc2c9ce9d1273b14715)
## Orders
### InOrder traversal
Left-to-right
- First visit the left subtree,
- Then the root,
- Then the right subtree.

Example:
```
__left___ 10, __right__

__,5,__, 10, ___ 21 __

1, 5, 7, 10, 16, 21, 25

Answer: [1,5,7,10,16,21,25]
```

### preOrder Traversal
Pre implies the one before comes first, meaning root comes first
PreOrder traversal:
- First visit the root,
- Then the left subtree,
- Then the right subtree.

Example:
```
10, __left__, ___right___

10, 5,_left_, _right_, 21, left_,right_

10, 5, 1, 7, 21, 16, 25

Answer: [10,5,1,7,21,16,25]
```

### Post Order Traversal
Order (root) is post

PostOrder traversal:
- First visit the left subtree,
- Then the right subtree.
- Then the root

Example:
```
__left__, ___right_, 10

_left_, right_, 5, _left_, _right_,21, 10

1, 7, 5, 16, 25, 21, 10

Answer: [1,7,5,16,25,21,10]
```

## Implementations
- Depth first search is used with a stack to process notes until the branch ends, used for nearest solutions
- [Breadth First Search](out/breadth-first-search.md)
- [T](None)
___

# Backlinks
```dataview
list from [Binary Tree Traversal](out/binary-tree-traversal.md) AND !outgoing([Binary Tree Traversal](out/binary-tree-traversal.md))
```
___
References:

Created:: 2021-11-10 14:53
