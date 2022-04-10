---
title: Set Operations
---
Status: 
Tags: 
Links: [Discrete Mathematics](out/discrete-mathematics.md)
___
# Set Operations
Operations can be expressed visually through [Set Venn Diagrams](out/set-venn-diagrams.md)
## Logics vs Sets
[![Image from Gyazo](https://i.gyazo.com/efddbd171315848c725f579e0ec57139.png)](https://gyazo.com/efddbd171315848c725f579e0ec57139)
[![Image from Gyazo](https://i.gyazo.com/6ebf6abdbdeef51a734ca88d3da3b076.png)](https://gyazo.com/6ebf6abdbdeef51a734ca88d3da3b076)
[![Image from Gyazo](https://i.gyazo.com/451630c8c3871a8abef4f2f8b6405966.png)](https://gyazo.com/451630c8c3871a8abef4f2f8b6405966)

## Set Notation
### Complements

Set that comprises all elements of U that do not belong to A
![Complement Set.excalidraw](out/excalidraw/complement-set.excalidraw.md)

### Intersections
?
![Drawing 2021-07-06 14.51.58.excalidraw](out/excalidraw/drawing-2021-07-06-14.51.58.excalidraw.md)
[![Image from Gyazo](https://i.gyazo.com/34c9c29c32224c64a3ff75d0c26ce97b.png)](https://gyazo.com/34c9c29c32224c64a3ff75d0c26ce97b)
Ex)
- {1,3,5,7} ∩ {2,3,4,5,6} = {3,5}

### Unions
?
[![Image from Gyazo](https://i.gyazo.com/4b2a2f239ba60d1dca0c53d0e7fe67cb.png)](https://gyazo.com/4b2a2f239ba60d1dca0c53d0e7fe67cb)
Ex)
- {1,3,5,7} ∪ {2,3,4,5,6} = {1,2,3,4,5,6,7}

### Differences
?
Include elements of A if not in B
[![Image from Gyazo|400](https://i.gyazo.com/494586dbc42e30d8848b421ec298c418.png)](https://gyazo.com/494586dbc42e30d8848b421ec298c418)
Ex)
- {1,3,5} - {1,2,3} = {5}

### Symmetric Differences
?
A∆B=(A-B) ∪(B-A)
[![Image from Gyazo](https://i.gyazo.com/1d0db63be2e1f0ea3d588888649f5b1c.png)](https://gyazo.com/1d0db63be2e1f0ea3d588888649f5b1c)
> [Cool Proof](https://youtu.be/-KQpyuaPs-E)e


### Disjoint Sets
?
A ∩ B = ∅

### Principle of Inclusion-Exclusion
?
[![Image from Gyazo](https://i.gyazo.com/d07c81496d8763f4d4a0fcbcea038572.png)](https://gyazo.com/d07c81496d8763f4d4a0fcbcea038572)
## Proofs
[ExamplesOfProofs.DVI (washington.edu)](https://sites.math.washington.edu/~aloveles/Math300Summer2011/ExamplesOfProofs.pdf)

###### Steps for proving equivalence a = b
?
- Prove that a implies b and b implies a
- Start with a, and manipulate to turn into b using definitions
- Start with b, manipulate to turn into a using definitions
- Thus, a = b


###### Prove $A - B = A n B^c$
?
[![Image from Gyazo](https://i.gyazo.com/a6a72e9a95343f54a3ea22c5ef7995d5.png)](https://gyazo.com/a6a72e9a95343f54a3ea22c5ef7995d5)
###### Sets A and B are disjoint if and only if A ∪ B = A ∆ B
?
Proof
[![Image from Gyazo](https://i.gyazo.com/529cbe6007646a90998df5aafbab80d5.png)](https://gyazo.com/529cbe6007646a90998df5aafbab80d5)
###### DeMorgan's Law in Set Notation
[![Image from Gyazo](https://i.gyazo.com/f664a62cdc227d9736eb0d64b1315a00.png)](https://gyazo.com/f664a62cdc227d9736eb0d64b1315a00)
###### DeMorgan's Law using set builder and logic
[![Image from Gyazo](https://i.gyazo.com/733372a34a2aea42d721579fdceda4e3.png)](https://gyazo.com/733372a34a2aea42d721579fdceda4e3)
___
# Backlinks
```dataview
list from [Set Operations](out/set-operations.md)
```
___
References: 

Created:: 2021-07-06 14:07
