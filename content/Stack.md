---
title: Stack
---
Status: 
Tags: #cards/cmpt225/dataStructures
Links: [Abstract Data Type](out/abstract-data-type.md)
___
# Stack
## Principles
An ordered collection of items
- `push(item)`add an item to the stack
- `pop()` remove item, return value
- `peek()` check top item
- `isEmpty()` checks if stack is empty
- Last-in-first out (LIFO)
	- ex) Undo button (ctrl+z)
### Use Cases
- Compiler
	- Checking for balanced braces while parsing code to verify syntax
- Evaluating postfix expressions
- Finding way through maze
- undo/redo buttons
- Simulate recursive operations
### Big O Notation
- Array-based, all is O(1)
- Link-based, all is O(1) except for popAll, O(n)
## Implementations

### using List
- Top is next available loc
- keep top open

isEmpty()
- check elementCount

push()
- if empty make new list
- if top is front, insert(1, elem)
- if top is back, insert(elemCount+1, elem)

pop()
- top = front, remove(1)
- top = back, remove(elements->getElementCount())

Advantages
- Simple implementation
- List ADT already tested then its good

Disadvantages
- Not guaranteed O(1) efficiency


___
# Backlinks
```dataview
list from [Stack](out/stack.md) AND !outgoing([Stack](out/stack.md))
```
___
References:

Created:: 2021-10-27 14:49
