---
title: Linked List
---
array vStatus: 
Tags: 
Links: [Abstract Data Type](out/abstract-data-type.md)
___
# Linked List
## Principles
- Each elem is linked to following like a chain
- List has a head
- Last elem points to null
- When adding, you must start at the head
### Characteristics
#### Single vs double
- Head vs head + tail

#### Single vs doubly linked
- Next vs next + prev
- helps make some operations O(1) if DHDL

#### Circular
- tail->next = head
- head->prev = tail
#### Sorting type
##### Position-oriented
- position is passed as parameter
##### Value-oriented data
Two possibilities:
- insert in sort order using a search key, O(n)
- Prepend then sort list, O(nlogn)
	- Yucky!!
### Traversing
In relation to removing the last node:
- `previous` local pointer
	- Store previous node, keep going until `curr->next == NULL`
	- set `previous` as tail, `delete curr`
- Look ahead
	- `next->next` to check if null
	- must attend to empty + 1 node case
- prev pointer in node structure
## Syntax
### Functions
`add_to_head`
`add_to_tail`
`remove_from_head`
`remove_from_tail`
### Variables
`list->head`
`node->next`
`node->data`
## Implementation
- Have a var that stores pointer of next item
   
```c
struct node{ 
	int data; 
	struct node * next;  
};

typedef struct node node_t;  

node_t x1;  
x1.data = 5;

x1.next = NULL;

node_t x2;  
x2.data = 7;

x1.next = &x2;

x2.next=NULL;
```
### Add to Head

- Create new node, set next of new node to old head

New list:
```cpp
append(int newElement) {
    Node * newNode = new Node(newElement);
    if (newNode != NULL) {
      if (head == NULL) head = newNode;
      else {
        // Move to the end of the list
        Node * current = head; // Anchor
        while (current -> next != NULL)
          current = current -> next;
        current -> next = newNode;
      }
      elementCount++;
    }
}

```

### Remove from Head
```c
if (head != NULL) {
Node* nodeToRemove = head;
head = head->next;
// Return node to the system
nodeToRemove->next = NULL;
delete nodeToRemove;
nodeToRemove = NULL;
elementCount--;
}
___
# Backlinks
```dataview
list from [Linked List](out/linked-list.md) AND !outgoing([Linked List](out/linked-list.md))
```
___
References:

Created:: 2021-11-01 15:21
