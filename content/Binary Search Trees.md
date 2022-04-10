Status: 
Tags: #cards/cmpt225/dataStructures/trees
Links: [[Rooted Tree|Binary Tree]]
___
# Binary Search Trees
- inOrder traversal prints elements in increasing order
## Principles
### Utilities
- Insert
- Remove
- Retrieve
- Traverse
- getElementCount
### Types
Degenerate binary search tree
?
- Worst case scenario where it is line

### Time Efficiency

[[Self-balancing binary search tree]]
### Implementations
#### Array-Based 1
##### Visual Representation
[![Image from Gyazo](https://i.gyazo.com/267b9057665a9aa9fbc853d1af19e303.png)](https://gyazo.com/267b9057665a9aa9fbc853d1af19e303)
##### Code
```cpp
class BSTNode {
	private:
		ElementType element; // element stored in tree node
		int leftChild; // index to left child/subtree
		int rightChild; // index to right child/subtree
}

class BinarySearchTree {
	private:
		BSTNode myTree[CAPACITY];// array of tree elements
		int root; // index of root
		int elementCount; // number of elements
}
```
#### Array-Based 2
##### Visual Representation
[![Image from Gyazo](https://i.gyazo.com/57e7a69065a22cc361a5c601ef7e6dba.png)](https://gyazo.com/57e7a69065a22cc361a5c601ef7e6dba)
##### Code
```cpp
class BinarySearchTree {
	private:
		ElementType myTree[CAPACITY]; // array of elements
		int elementCount; // number of elements
}
```
#### Link-based
```cpp
class BSTNode { 
	private:
		ElementType element; // element stored in tree
		node BSTNode* leftChild; // link to left child/subtree
		BSTNode* rightChild; // link to right child/subtree 
}

class BinarySearchTree {
	private:
		BSTNode* root; // root of tree
		int elementCount; // number of elements
}
```

### Public Interface
#### insert()
- wrapper function
	- validate params, prepare new params, call recursive private method `insertR()`
##### insertR()
```cpp
Node* BST::insertR(Node* subTree, Node* newNode){
	if (subTree == NULL) return newNode; // Base case
	else
	{
		if (subTree->getElement() > newNode->getElement())
		subTree->setLeft(insertR(subTree->getLeft(), newNode));
		else
		subTree->setRight(insertR(subTree->getRight(),newNode));
	return subTree;
} // end if
}

```


## Functions
### find
```c
BTnode_t* recursive_find (BTnode_t* root, int item) {
	if ( root == NULL )
		return NULL;
	if (root->value == item)
		return root;
	if ( root->value > item )
		return find( root->left, item) ;
	else // if ( root->data < item )
		return find( root->right, item) ;
}


BTnode_t* iterative_find (BTnode_t* root, int item) {
 BTnode_t* current = root;
	while ( current != NULL && current->value != item) {
		if (current->value > item )
			 current = current->left;
		else  	// current->data < item
			current = current->right;
	}
	return current;
}
```
### remove
- Iterate to find elem, remove, connect child of elem as children of elem parent
	- If elem to be removed is root, find successor (next smallest elem), remove it, and replace it with the root
___
# Backlinks
```dataview
list from [[Binary Search Trees]] AND !outgoing([[Binary Search Trees]])
```
___
References:

Created:: 2021-11-15 14:52
