Status: 
Tags: 
Links: [[C Variables]] - [[C Pointers and References]]
___
# C Constant Pointers
const int* vs int* const
- `int* const` is a constant pointer
```
	int x, y;
	int* const const_ptr = &x;
	const_ptr = &y; // NO! Modifying the pointer is not allowed
```


- `const int*` is a pointer to a constant
	- Can point to non-const but cannot change
```
	const int x = 9;
    const int* ptr = &x;  
	*ptr = 8; // NO! Modifying the data is not allowed
```

___
# Backlinks
```dataview
list from [[C Constant Pointers]] AND !outgoing([[C Constant Pointers]])
```
___
References:

Created:: 2021-09-15 14:44
