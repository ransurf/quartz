---
aliases:
---
Status:
Tags: #cards/cmpt225/dataStructures/adt/trees
Links: [[Binary Tree]]
___

# Binary Heap

## Principles
Strength
?
- Finding element with largest/smallest key value

### Operations

#### `remove()`
[![Image from Gyazo](https://i.gyazo.com/53f09f8f6249b16170e0ab7d07dcac0f.png)](https://gyazo.com/53f09f8f6249b16170e0ab7d07dcac0f)
?
[![Image from Gyazo](https://i.gyazo.com/a7a8bb6c924d0e30a7211c303bc7516d.png)](https://gyazo.com/a7a8bb6c924d0e30a7211c303bc7516d)

### Time Efficiency
Overall: O($log_2n$)
Visit each level of heap ;; O($log_2n$)
Retrieval ;; O(1)

### Public Interface
```cpp
// Description: Inserts an element.
bool insert( ElementType ) ;
// Description: Removes the element located at the root and returns it.
// Precondition: Binary heap is not empty.
// Throws EmptyBinaryHeapException if binary heap is empty.
ElementType remove( );
// Description: Returns the element located at the root.
// Precondition: Binary heap is not empty.
// Postcondition: The binary heap is unchanged by this operation.
// Throws EmptyBinaryHeapException if binary heap is empty.
ElementType max( ) const;
ElementType min( ) const;
// Description: Returns the number of elements stored in the data collection.
// Postcondition: The binary heap is unchanged by this operation.
int getElementCount( ) const;
```

### Types

#### Minimum Binary Heap
?
- Complete binary tree
- Key value of anode in such heap is < or = to key value of its children
- Node's let and right subtrees are also minimum binary heaps
- root contains the element with the smallest key value

##### Operations

###### `insert()`
Algorithm for Max Binary Heap
?
```cpp
indexOfRoot = 0
indexOfBottom = elementCount
insert new element @ “bottom” of heap(@ indexOfBottom)
elementCount++
reHeapUp(indexOfBottom)
// If the element has a parent and …
if (indexOfBottom > indexOfRoot)
  indexOfParent = floor((indexOfBottom– 1) / 2)
// … key value of parent < key value of child then …
if (heap[indexOfParent] > heap[indexOfBottom])
  //… swap the element with its parent
  swap heap[indexOfParent] with heap[indexOfBottom]
reHeapUp(indexOfParent)
```
[![Image from Gyazo](https://i.gyazo.com/6158a00293dd705ae5e14900537eac33.png)](https://gyazo.com/6158a00293dd705ae5e14900537eac33)

###### `remove()`
```cpp
int MinHeap::extractMin()
{
	if (heap_size <= 0)
		return INT_MAX;
	if (heap_size == 1)
	{
		heap_size--;
		return harr[0];
	}

	// Move last element to first then reHeapDown
	int root = harr[0];
	harr[0] = harr[heap_size-1];
	heap_size--;
	MinHeapify(0);

	return root;
}
```

#### Maximum binary heap
?
- Complete binary tree
- key value of a node in such heap is > or = to key value of its children (if any)
- the node’s left and right subtrees are also maximum binary heaps
- root contains the element with the largest key value

##### Operations

###### `insert()`
Algorithm for Max Binary Heap
?
```cpp
indexOfRoot = 0
indexOfBottom = elementCount
insert new element @“ bottom” of heap(@ indexOfBottom)
elementCount++
reHeapUp(indexOfBottom)
// If the element has a parent and …
if (indexOfBottom > indexOfRoot)
  indexOfParent = floor((indexOfBottom– 1) / 2)
// … key value of parent < key value of child then …
if (heap[indexOfParent] < heap[indexOfBottom])
  //… swap the element with its parent
  swap heap[indexOfParent] with heap[indexOfBottom]
reHeapUp(indexOfParent)
```

###### `remove()`
```cpp
indexOfRoot = 0
call retrieve()(optional) =>
  return element stored in root of heap(array[indexOfRoot])
replace element stored in root with element stored at the bottom of
  heap i.e., last element => copy element stored at the bottom(at index elementCount - 1)
into root of heap => elementCount–
reHeapDown(indexOfRoot)
// If the parent has at least a child and …
if (heap[indexOfRoot] is not a leaf)
  compute index of children
compare the children and pick largest child
set indexOfMaxChild to index of largest child of root
// … key value of parent < key value of largest child then …
if (heap[indexOfRoot] < heap[indexOfMaxChild])
  //… swap the parent with its largest child
  swap heap[indexOfRoot] with heap[indexOfMaxChild]
reHeapDown(indexOfMaxChild)
```

### Implementations

#### Array
- Of a cell at index i:
	- Left child is located index 2*i + 1
	- Right child is located at index 2*i + 2
	- Parent is located at index floor( (i-1) / 2)

Last parent is stored
?
- floor([eC/2] - 1)

### Algorithms

#### reHeapUp
```cpp
// Utility method - Recursively put the array back into a min Binary Heap.
template <class ElementType>
void BinaryHeap<ElementType>::reHeapUp(unsigned int indexOfBottom) {

	if(indexOfBottom > 0) {
		int indexOfParent = floor((indexOfBottom - 1) / 2);
		if(elements[indexOfBottom] <= elements[indexOfParent])
		{
			//Swap
			ElementType temp = elements[indexOfParent];
			elements[indexOfParent] = elements[indexOfBottom];
			elements[indexOfBottom] = temp;
			reHeapUp(indexOfParent);
		}
	}

	return;
	
} // end reHeapUp
#### reHeapDown
```cpp
template <class ElementType>
void BinaryHeap<ElementType>::reHeapDown(unsigned int indexOfRoot) {

	unsigned int indexOfMinChild = indexOfRoot;
	
	// Find indices of children.
	unsigned int indexOfLeftChild = 2*indexOfRoot+1;
	unsigned int indexOfRightChild = 2*indexOfRoot+2;

    // Base case: elements[indexOfRoot] is a leaf as it has no children
	if (indexOfLeftChild > elementCount-1) return;

	// If we need to swap, select the smallest child
    if (elements[indexOfRoot] > elements[indexOfLeftChild])
    	indexOfMinChild = indexOfLeftChild;

    // Check if there is a right child, is it the smallest?
    if (indexOfRightChild < elementCount) {
		if (elements[indexOfMinChild] > elements[indexOfRightChild])
		    indexOfMinChild = indexOfRightChild;
	}

	// Swap parent with smallest of children.
	if (indexOfMinChild != indexOfRoot) {
		
	   ElementType temp = elements[indexOfRoot];
	   elements[indexOfRoot] = elements[indexOfMinChild];
	   elements[indexOfMinChild] = temp;
	   
	   // Recursively put the array back into a heap
	   reHeapDown(indexOfMinChild);
    }

	return;
	
} // end reHeapDown
___
References:

Created:: 2022-03-14 05:29
