Status: 
Tags: #cards/cmpt225/dataStructures/hash 
Links: [[Collusion resolution strategies]]
___

# Closed Addressing
- See [[Hashing#Closed Addressing Chain Hashing|implementations]] for hash map
## Principles
- Elements are not stored in hash table itself
- Structure is mix of bounded and unbounded data structures

Structure (sections)
?
- Section 1: bounded
	- Array for direct indexing
	- Instead of storing element, stores a chain
- Section 2: Unbounded
	- Data structure such as linked list, etc
	- Actually contains elements

##### Chaining
?
[![Image from Gyazo](https://i.gyazo.com/cf549445d10ce48de284c3ffec6f94b6.png)](https://gyazo.com/cf549445d10ce48de284c3ffec6f94b6)
length of chain < length of cluster < n
___
References:

Created:: 2022-03-30 18:10
