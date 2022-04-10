---
title: List Data Collection
aliases:
---
Status:
Tags: #cards/cmpt225/dataStructures
Links: [Abstract Data Type](out/abstract-data-type.md)
___

# List Data Collection

## Principles
### Implementation
Array-based
```c
class List {
private:
	static const int INITIAL_SIZE = 5;
	int elements[INITIAL_SIZE];
	// or
	int* elements;
	int elementCount;
	int capacity;
public:
	~List() {
		delete[] elements;
	}
}
### Operations
> capitalized ones are only for pos-oriented, not value
```cpp
// insert an element at a given position in the list
insert(element, POSITION);
// append an element at the end of the list
APPEND(element);
// remove the element at a given position in the list
remove(position);
// remove all the elements from the list
removeAll();
// get the element at a given position in the list
elementType get(position);
// swap two elements
SWAP(position1, position2);
// how many elements are in the list
int getElementCount();
```
___
References:

Created:: 2022-03-07 21:13
