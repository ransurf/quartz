Status: 
Tags: 
Links:
___

# Disk Bound Data
## Principles
- External storage

### Blocks
- Basic unit written to/read from external storage (disk)
	- Files are made of blocks
- 1kb to 64kb, in Linux it is 1024 bytes

### Modifying info on a hard drive
Steps:

1. must access first
	- Hard drive access time is $10^{-3}$
	- Memory access time is $10^{-9}$
	- Million to one ratio
2. Repeat until right data retrieved

### Types
Unsorted
Sorted
Index file implementation
- Index file that contains AVL nodes
	- Each node contains:
	- element of node has indexing key (ex. SIN)
	- data file block number
	- Location of left sub-tree
	- Location of right sub-tree
___
References:

Created:: 2022-04-04 20:13
