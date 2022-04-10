Status: 
Tags: 
Links: [[C MOC]]
___
# C Memory Allocation
- To initialize right size of array on runtime, dynamic memory allocation is needed
- Since pointer is saved, array can be used outside of function !
## Practices
- malloc
	- return type `void*` (needs typecating)
	- returns null if allocation fails
	- release memory after
		- releasing: `free(arr)`
		[Array malloc example](https://replit.com/@JohnReyes08/VirtualSubduedTexts#main.c:5:1)
## Functions

### realloc
Expands or contracts the existing area pointed to by ptr, copying to new location
- If fails, returns null

```c
void* realloc(void *ptr, size_t size) 
```
### memcpy
```c
void* memcpy(void * dest, const void* source, size_t num) 
// copies the values of num bytes from a source to dest
```
### memset

```c
void * memset(void * ptr, int val, size_t num) 
// sets the first num bytes in memory to be val
```
### calloc

```c
void * calloc(int num_of_items, int size) 
// allocates num_of_items objects of the specified size
// in the memory and sets the memory to 0 
// essentially equivalent to 

void * ptr = malloc(num_of_items*size);
memset(ptr, 0, num_of_items*size); 
```
## Syntax
```c
(void *) malloc(size_t) 
	// allocates size_t consecutive bytes in memory
	// size_t alias for unsigned integer type 

// ======= Usage =======

int * array = (int*) malloc(n * sizeof(int));
```
___
# Backlinks
```dataview
list from [[C Memory Allocation]] AND !outgoing([[C Memory Allocation]])
```
___
References:

Created:: 2021-09-27 15:40
