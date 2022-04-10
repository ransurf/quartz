---
aliases:
---
Status:
Tags: #cards/cmpt225/dataStructures
Links: [[Data Structures]]
___

# Hashing

## Principles
?
- Instead of a 1:1 mapping, you do a hashing process to reduce the size of the image using [[Hash Functions]]

Load factor
?
- Sigma symbol
- \# of elements (n) / size of hash table (B)
- *ex) 1 = full hash table*

### Collisions
?
When multiple unique index keys are hashed to the same locations in the hash table
- many to 1 mapping

Preventing collisions
?
- Easy to compute hash functions that easily distribute the indexing keys
- [[Collusion resolution strategies]]
- Size of hash table
- Average length of each chain in closed addressing

### Downsides
?
- Not good for constantly finding min/max, or sort order retrieval

### Insert/Search/Remove
#### Open Addressing

##### Scenarios

###### Scenario 1, Empty
1. Compute hash index h(k)
2. Probe the resulting location (i.e. cell) in hash table, see it's empty
3. Cases
	- Insertion
		- insert since empty
	- Search
		- Not found
	- Remove
		- None to remove

###### Scenario 2, Same Element In
1. Compute hash index h(k)
2. Probe the resulting location (i.e. cell) in hash table, see it's filled
3. Cases
	- Insertion
		- Already inserted
	- Search
		- Found
	- Remove
		- Labelled `ToBeDelete`, needed to find other elements

###### Scenario 3, Diff Element In
1. Compute hash index h(k)
2. Probe the resulting location (i.e. cell) in hash table, see it's filled
3. Cases
	- Insertion
		- [[Open Addressing]]
	- Search
		- Found
	- Remove
		- Labelled `ToBeDelete`, needed to find other elements

###### Scenario 4, All Locations Probed
- Expand hash table
- Tweak hash function to map new range of hash indexes
- Re-insert into new table using new hash function

##### Disadvantages
- 0-50% O(1)
- 50% full primary cluster starts to form
- 70% ful performance becomes O(n)

#### Closed Addressing (Chain Hashing)

Inserting into a chain
?
- H(k) = index
- Add element to chain `insertFirst()`
- Time efficiency: O(1)

Searching a chain
?
- H(k) = index
- Traverse chain (looking for key)
- If "key" not in an element of chain, then element not in hash table
- Time efficiency: O(1+sigma)

###### Example
SHSL list, prepend()
[![Image from Gyazo](https://i.gyazo.com/56e23e91018b2816e4c6e84665a5bd41.png)](https://gyazo.com/56e23e91018b2816e4c6e84665a5bd41)
?
[![Image from Gyazo](https://i.gyazo.com/15185a1be15950c67cef3e4c1cca74b8.png)](https://gyazo.com/15185a1be15950c67cef3e4c1cca74b8)

___
References:

Created:: 2022-03-22 19:50
