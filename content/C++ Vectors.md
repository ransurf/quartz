Status: 
Tags: 
Links: [[C++ MOC]]
___
# C++ Vectors
- Adding something to a vector creates a copy
## [Iterating through a vector](https://stackoverflow.com/questions/12702561/iterate-through-a-c-vector-using-a-for-loop)
```cpp
for(std::vector<T>::size_type i = 0; i != v.size(); i++) {
    v[i].doSomething();
}

// print those elements
for (auto it = v.begin(); it != v.end(); ++it){
    std::cout << *it << std::endl;
}
```

___
# Backlinks
```dataview
list from [[C++ Vectors]] AND !outgoing([[C++ Vectors]])
```
___
References:

Created:: 2021-11-28 17:12
