---
title: C++ Exceptions
---
Status: 
Tags: 
Links: [C++ MOC](out/c-moc.md)
___

# C++ Exceptions
## Principles
- Create function that us child class of `logic_error`
	- Has params for string message to throw
	- Calls `logic_error` that prints type of exception and message param

try / catch
- Wrap `try` over potential exception code
- when exception happens, skip rest of try and goes to catch
```cpp
catch (ExceptionType& e) {
	e.what()
	//recovery
}
```
___
References: https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Labs/Lab6/6-operator_overloading_and_exceptions.html


Created:: 2022-03-01 04:09
