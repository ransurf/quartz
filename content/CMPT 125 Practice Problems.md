---
aliases:
---
Status:
Tags:
Links: [[CMPT 125 Studying]]
___

# CMPT 125 Practice Problems
- Use the big-O notation to express the running time of bar(n) as a function of n
- Write a function with the same functionality as bar(n) whose running time is O(1).
## Binary Search Trees
3,4 - far left/far right
5- In-order traversal
6- 
7- if statement before printing
8- 
9- 
11- 
16- 
## [Binary Trees](https://piazza.com/class/kt82u06t98j7fd?cid=220)

### 1 - Equality of two binary trees
`src16`
```c
bool BT_equal(BTnode_t* root1, BTnode_t* root2) {
  
 if (root1 == NULL || root2 == NULL) {

 return true;

 }
  
 bool isEqual = true;

 if (root1->value != root2->value) {

 isEqual = false;

 }
  
 return BT_equal(root1->left, root2->left) && isEqual && BT_equal(root1->right, root2->right);

}
```

### 2 - Array to inOrder
```c
BTnode_t* in_order_tree(int* arr, int n) {
  
 BTnode_t* parent = create_node(arr[0]);
  
 for (int i = 1; i<n; i++) {
	 BTnode_t* child = create_node(arr[i]);
	 set_right_child(parent, child);
 }
	
 return parent;
}
```

### 3 - Iterative Size
```c
int iterative_tree_size(BTnode_t* root) {

  if (root == NULL) {
    return 0;
  }

  LL_t* list = LLcreate();
  int size = 0;
  LL_add_to_head(list, root);
  
  while (list->size > 0) {
    BTnode_t* curr = list->head->data;

    if (curr->left != NULL)
      LL_add_to_tail(list, curr->left);

    if (curr->right != NULL)
      LL_add_to_tail(list, curr->right);

    LL_remove_from_head(list);
    size++;

  }

  return size;
}
```
### 4 - 
### 5 - Nodes in level k
Only prints but still works :p
```c
void nodes_in_level(BTnode_t* root, int n) {
  if (root == NULL)
    return;

  if (n==0)
    printf("%d\n", root->value);
  
  else {
    nodes_in_level(root->left, n-1);
    nodes_in_level(root->right, n-1);
  }
}
```

## [Stacks, Queues, LL](https://piazza.com/class/kt82u06t98j7fd?cid=178)
### 1 - get_middle
```c
node_t* get_middle(LL_t* list) {

  node_t* newNode = (node_t*) malloc(sizeof(node_t));

  int mid = list->size/2;

  newNode = list->head;

  for (int i=0; i<mid; i++) {
    newNode = newNode->next;
  }
  
  return newNode;
}
```
### 2 - equal_lists
```c
bool are_equal(const LL_t * list1, const LL_t * list2) {

  if (list1->size != list2->size) {
    return false;
  }

  int i = 0;
  node_t* elem1 = list1->head;
  node_t* elem2 = list2->head;

  while (elem1 != NULL) {
    if (elem1->data != elem2->data)
      return false;
    elem1 = elem1->next;
    elem2 = elem2->next;
  }
  return true;
}
```
### 3 - copy_list
```c
LL_t* copy_list(LL_t* orig) {
	
	LL_t *new_list = LLcreate();
	node_t* orig_node = orig->head;
	
	//new_list->head = orig_node;
	while(orig_node != NULL){
		LL_add_to_tail(new_list,orig_node->data);
		//printf("%d\n",orig_node->data);
		orig_node = orig_node->next;
	}
	return new_list;
}
```

### 4 - equal_queues
- Create size helper function
- src14/queue-LL
```c
int queue_size(queue_t* queue) {

  queue_t* temp_q = queue_create();
  int size = 0;

  while (!queue_is_empty(queue)) {
    enqueue(temp_q, dequeue(queue));
    size++;
  }

  while (!queue_is_empty(temp_q)) { //put back into original stack
    enqueue(queue, dequeue(temp_q));
  }

  queue_free(temp_q);
  return size;
}

bool equal_queues(queue_t* q1, queue_t* q2) {
  
  queue_t* temp_1 = queue_create();
  queue_t* temp_2 = queue_create();

  int size1 = queue_size(q1);
  int size2 = queue_size(q2);

  if (size1 != size2) { 
    queue_free(temp_1);
    queue_free(temp_2);
    return 0;
  }
  
  while (!queue_is_empty(q1)) { //check for equality, store all values

    int q1curr = dequeue(q1);
    int q2curr = dequeue(q2);
    printf("gets vals");

    if (q1curr != q2curr) {
      queue_free(temp_1);
      queue_free(temp_2);
      return 0;

    } else {
      enqueue(temp_1, q1curr);
      enqueue(temp_2, q2curr);
    }
  }

  while (!queue_is_empty(temp_1) ) { //put back into original queues

    int data = dequeue(temp_1);
    enqueue(q1, data);
    data = dequeue(temp_2);
    enqueue(q2, data);
  }

  queue_free(temp_1);
  queue_free(temp_2);

  return 1;
}
```

### 5 - copy_queue
```c
queue_t* copy_queue(queue_t* orig) {
  queue_t* copy_q = queue_create();
  queue_t* temp_q = queue_create();

  while (!queue_is_empty(orig)) {
    enqueue(temp_q, dequeue(orig)); //put into temp
  }

  while (!queue_is_empty(temp_q)) {
    int data = dequeue(temp_q); //allows to build both
    enqueue(orig, data);
    enqueue(copy_q, data);
  }

  return copy_q;
}
```

### 6 - equal_stacks
```c
int stack_size(stack_t* s) {
  // implement me
  stack_t* temp_stack = stack_create();
  int size = 0;

  while (!stack_is_empty(s)) {
    stack_push(temp_stack, stack_pop(s));
    size++;
  }

  while (!stack_is_empty(temp_stack)) { //put back into original stack
    stack_push(s, stack_pop(temp_stack));
  }

  stack_free(temp_stack);
  return size;
}

bool stack_equal(stack_t* s1, stack_t* s2) {
  // implement me
  stack_t* temp_1 = stack_create();
  stack_t* temp_2 = stack_create();
  int size1 = stack_size(s1);
  int size2 = stack_size(s2);

  if (size1 != size2) { 
    stack_free(temp_1);
    stack_free(temp_2);
    return 0;
  }

  while (!stack_is_empty(s1)) { //s1 and s2 have to be same size due to above return if conditional

    int val1 = stack_pop(s1);
    int val2 = stack_pop(s2);
    

    if (val1 != val2) {
      stack_free(temp_1);
      stack_free(temp_2);
      return 0;
    } else {
      stack_push(temp_1, val1);
      stack_push(temp_2, val2);
    }
  }
 
  while (!stack_is_empty(temp_1)) { //put back into original stacks
    
    int data = stack_pop(temp_1);
    stack_push(s1, data);
    data = stack_pop(temp_2);
    stack_push(s2, data);
  }
  
  stack_free(temp_1);
  stack_free(temp_2);
  
  return 1;
}
```

### 7 - copy_stack
```c
stack_t* copy_stack(stack_t* orig) {
	stack_t* copy_s = stack_create();
	stack_t* temp_s = stack_create();
	
	while (!stack_is_empty(orig)) {
		stack_push(temp_s, stack_pop(orig));
	}
	
	while (!stack_is_empty(temp_s)) {
		int data = stack_pop(temp_s);
		stack_push(orig, data);
		stack_push(copy_q, data);
	}
	return copy_s;
}
```

### 8 - reverse_queue
```c
void reverse_queue(queue_t* queue) {

  LL_t* list = malloc(sizeof(LL_t)); //temp to store in reverse
  LLcreate(list);

  while (!queue_is_empty(queue)) { //adds to head to reverse
    int data = dequeue(queue);
    LL_add_to_head(list, data);
    

  }
 

  while (list->head != NULL) {
    int data = LL_remove_from_head(list);
    enqueue(queue, data);
    printf("qdata = %d\n", data);
  }

  LL_free(list);
}
```

### 9 - reverse_stack
```c
void reverse_stack(stack_t* stack) {
  stack_t* temp_s = stack_create();
  stack_t* temp_s2 = stack_create();

  while (!stack_is_empty(stack)) {
    stack_push(temp_s, stack_pop(stack));
  }

  while (!stack_is_empty(temp_s)) {
    stack_push(temp_s2, stack_pop(temp_s));
  }

  while (!stack_is_empty(temp_s2)) {
    stack_push(stack, stack_pop(temp_s2));
  }
}
```

### 10
Enqueue - push onto s1
Dequeue - push s1 -> s2, pop s2, push s2 -> s1
isEmpty - check if stack is empty

### 11

### 12

## [Basics of Coding in C](https://piazza.com/class/kt82u06t98j7fd?cid=22)
> 14 Questions
- [[CMPT 125 Basics of Coding in C Practice Problems]]

### Attempts
- [x] 2- prints `a` twice
- [x] 3- Doesn't run
- [ ] 4- Either prints 'a' twice or error due to modifying constant pointer
- [x] 5- Did it mentally then in code, holy I am slow lmao
- [ ] 6-
- [ ]

### Answers
2- Yup
3- Runs on gcc, but not on replit???
4- Error
5- Yes, just need to brush up on syntax

## Big O Notation
- CMPT125-Midterm Review on Piazza
- [[CMPT 125 Big O Notation Practice Problems]]

## [Dynamic Memory Allocation](https://piazza.com/class/kt82u06t98j7fd?cid=69)
> 6 Questions

## Recursion
- [[CMPT 125 Recursion Practice Problems]]

## [Searching and Sorting](https://piazza.com/class/kt82u06t98j7fd?cid=103)
- [[CMPT 125 Searching and Sorting Practice Problems]]
___

# Backlinks
```dataview
list from [[CMPT 125 Practice Problems]] AND !outgoing([[CMPT 125 Practice Problems]])
```
___
References:

Created:: 2021-10-17 16:13
