---
title: C++ Object Oriented Programming
---
Status: 
Tags: 
Links: [C++ MOC](out/c-moc.md)
___
# C++ Object Oriented Programming
- `new` mallocs and calls constructor
	- Be sure to delete in the end as it's not local/on the stack

- virtual is override
- Can send through values
- Copy constructors help create variables in parameters
## Methods
https://www.w3schools.com/cpp/cpp_class_methods.asp
```cpp
// Method/function definition outside the class  
void **MyClass::myMethod()** {  
 cout << "Hello World!";  
}
```
## Constructors
- Copy constructors are called when you have a function that returns a value rather than returns a pointer
	- Returning a value will require a copy as you are not trying to return the reference

```cpp
//outside definition
Car::Car(string x, string y, int z) {  
 brand = x;  
 model = y;  
 year = z;  
}
// Creating new object
Car carObj1("BMW", "X5", 1999);
//empty constructor call
Car carObj2;
```
___
# Backlinks
```dataview
list from [C++ Object Oriented Programming](out/c-object-oriented-programming.md) AND !outgoing([C++ Object Oriented Programming](out/c-object-oriented-programming.md))
```
___
References:

Created:: 2021-11-22 15:53
