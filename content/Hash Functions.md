---
aliases:
---
Status:
Tags:
Links: [[Hashing]]
___

# Hash Functions

## Principles
?
- Easy to compute
- O(1)
- Even distribution of indexing keys across range of array indices

### Types
#### Modular arithmetic
?
- Use modulo operator %
- Usually used as last step of a hash function, `key % arraySize` to make sure it's possible

#### Folding
?
- Parition indexing key into parts and combining these parts using artihmetic operations
- *ex) with a 16 digit number, you can split into 6 digits and 2x 5 digits, then use sum as index*

Types of folding
?
- Shift
	- Group then add
- Boundary
	- Alternate sections are reversed
		- *ex) Second parition would have its order reversed*

#### Truncation
?
- Use only parts of indexing key unique to element
- Use modulo and division to isolate unique parts of a keyddd

#### Using strings/characters as indexing keys
?
- Apply arithmetic operations on the numerical code of each character

### Troubleshooting

Same values but rearranged differently
?
- Apply different weights onto values

Collision
?
- Multiple distinct keys are hashed to same location in the hash table
	- Called synonyms

___
References:

Created:: 2022-03-22 20:0