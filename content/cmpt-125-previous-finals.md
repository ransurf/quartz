---
title: CMPT 125 Previous Finals
---
Status: 
Tags: 
Links: [~ CMPT125 Finals Study Plan](out/~-cmpt125-finals-study-plan.md)
___
# CMPT 125 Previous Finals
## 2020
### 1
- a
	- [ ] cant comprehend this induction wtf
	- he just used induction to explain how the program works, which makes sense
- b
	- local copy from function does not result in changes
	- when theres potential for garbage values, say that it has a chance to work as intended but can also be undefined/not guaranteed
		- should mention local variable in my answer
			- since most recent local val created was 6,7, would probably print that
### 2
#### 
- actually forgot to  return and didnt properly use pred function...
	- problems of rushing
#### c
The function moves each node of cur into lists of either less or greater, and concatenates the two lists so less is always before >=
- tmp is required as cur->next would be altered 
```c
LL_node_t * rearrange(LL_node_t * head, int pivot) {
    LL_node_t * cur = head;
    LL_node_t * less = NULL; // pointer to the sublist with data<pivot
    LL_node_t * greater = NULL; // pointer to the sublist with data>=pivot
    LL_node_t * tmp;
    while (cur) {
      tmp = cur -> next;
      if (cur -> data < pivot) { // add cur to the less list as head
        cur -> next = less;
        less = cur;
      } else { // cur->data >= pivot
        cur -> next = greater; // add cur to the greater list
        greater = cur;
      }
      cur = tmp;
    }
    // here less is the sublist with all elements<pivot
    // greater is the sublist with all elements>=pivot
    // next we concatenate them
    if (less == NULL)
      return greater;
	
    cur = less; // less is non-empty
    while (cur -> next != NULL) // we iterate to the end of the list less,
      cur = cur -> next; 
    cur -> next = greater; // and add to the tail of the list to greater
    return less;
```
### 3
- [ ] evens and odds??
### 4
- just some minor hiccups, like forgetting about pointer being null, not properly attending to size, and 1 more i forget
## 2019
### 1
- a didn't start at 1 for the tmp string, at least i know how to swap now though lul
- c should state that it compiles, i guess setting a string works lmao
- d wrong math, didnt explain, just do recursion next time
	- forgot to account for bar(1) call
	- setup recurrence relation, ig it was squared not 2logn oops
- e idk man, should see the definitions on the slides then as this happens once per exam
### 2
- a,b don't know struct notation lmao
	- what's the point of the 2nd name tho??? im confused
- c,d is it necessary to return null?
- e no need for the null check as list->head would just be null
- f forgot to free welp

- b how is it possible for list to be accessed without referencing the stack given, why shouldn't it be stack->list instead?
- flag = 1 - flag is how to get boolean with int
- what would happen if you didnt implement the flag? would you get partial marks for all functions?
### 3
- a) damn it really is the size of the tree fk
	- base it off of many nodes it accesses
- b) Need to base it off of principles of bst, not just the one given
	- Should have figured that it was not just that since it was 10 marks
- 
## 2018
48/80
### Thoughts
- I guess I need to be more cautious with the logical part
	- At least my pointers are on point now B)
- Lots of straight up 0's, cant let that happen next time though
### 1
logic questions
- knowing what the function does, sucky at recursion
- Need to be more careful on stating definitions
### 2
- c quicksort big o notation, forgot worst case was O(n^2) and didnt show any work
- i had a hunch it was binary search fk, just didnt know how to change it to use it
### 3
- Ofc there was a non brute-force method, I wonder if this was covered in the class or not
	- Stopped listening cuz everything sounded the same
		- Didn't even realize it was a bst wtf, wouldve helped me know the proper order
- Always make room for null checks
- I hope polish and stuff isn't on the final xd
### 5
- Kinda cheated for first two, 17 is being generous
- Remember to free oops
___
# Backlinks
```dataview
list from [CMPT 125 Previous Finals](out/cmpt-125-previous-finals.md) AND !outgoing([CMPT 125 Previous Finals](out/cmpt-125-previous-finals.md))
```
___
References:

Created:: 2021-12-11 22:19
