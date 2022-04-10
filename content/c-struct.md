---
title: C Struct
---
Status: 
Tags: 
Links: [C Variables](out/c-variables.md)
___
# C Struct
- Set of data types?
- Can be passed and returned like a normal variable in functions
## Syntax
**Struct `student_info` with typedef `student`**
```c
struct student_info {  
 char* first_name;  
 char* last_name;  
 int ID;  
 int grades[5];  
};
typedef struct student_info student;

OR

typedef struct student_info {  
 char* first_name;  
 char* last_name;  
 int ID;  
 int grades[5];  
} student;
```

**Playing around with `student_info` struct**
```c
struct student_info studentVar; //defining variable
studentVar.first_name = "John";
student list_of_students[180];

list_of_students[10].first_name = "Jack";
```
**Using pointers with struct**
```c
student clark;  
 clark.first_name = "Clark"; 

  student* student_ptr = &clark;  
 (*student_ptr).last_name = "Kent"; // accessing a field in struct student_ptr->id = 123; // accessing a field in pointer to struct
```
___
# Backlinks
```dataview
list from [C Struct](out/c-struct.md) AND !outgoing([C Struct](out/c-struct.md))
```
___
References:

Created:: 2021-09-22 14:47
