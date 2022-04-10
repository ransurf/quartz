Status: 
Tags: #cards/cmpt225/dataStructures 
Links: [[Data Structures]]
___

# B-Tree
## Principles
Characteristics
?
- External data collection that organizes its blocks (B) into an m-way search tree
	- All leaves same level
	- root has at least 2 children (unless leaf node)
	- non-leaf nodes that are not root have at least floor(m/2) children
	- m is amount zmax amount of children
	- K = m-1, search key values in tree, sorted in ascending
	- All subtrees are in [![Image from Gyazo](https://i.gyazo.com/337ab7b4e62bf9b1364085814edb65a0.png)](https://gyazo.com/337ab7b4e62bf9b1364085814edb65a0)

### Data Collection
Used to organize index files as unlimited amount of pointer lessens depth of tree
- keys are index records
	- m pointers for index file block #videoidea/obsidian 
	- contains root of subtrees
### M-Way Search Tree


#### Diagram
m = 4 tree
K = m-1, search key values in tree, sorted in ascending
[![Image from Gyazo](https://i.gyazo.com/5423a1ea74e584667bdce99c47b88866.png)](https://gyazo.com/5423a1ea74e584667bdce99c47b88866)


___
References:

Created:: 2022-04-06 23:53
