Status: 
Tags: 
Links: [[C++ MOC]]
___
# C++ Templates
## Principles
- Make ADT store and manipulate data of any data type or of any class type
- When referenced in other classes, must be suffixed with `<ElementType>`
	- *ex) `Node<ElementType>* newNode = Node<ElementType>(newElement);`
### Requirements
- Preface the template class definition in _List.h_ with 
template \<class ElementType>
- Preface each template member method implementation in _List.cpp_ with template \<class ElementType> and replace the class qualifier Class:: that appears before the name of each method with Class\<ElementType>::
```cpp
template <class ElementType>
Class A {
	template <class ElementType>
	void A<class ElementType>::add(ElementType newElement){
}
```

## Syntax
- Instead of referencing just the object, you also reference <>
```

```
___
# Backlinks
```dataview
list from [[C++ Templates]] AND !outgoing([[C++ Templates]])
```
___
References: https://www2.cs.sfu.ca/CourseCentral/225/alavergn/Labs/Lab4/4-templates.html

Created:: 2022-02-01 22:56