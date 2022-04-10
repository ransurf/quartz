---
title: Open Addressing
aliases:
---
Status:
Tags: #cards/cmpt225/dataStructures/hash
Links: [Hash Functions](out/hash-functions.md)
___

# Open Addressing

## Principles
Effective open addressing
?
- Size hash table should not be even
	- Increase probability that each position is part of probing sequence
		- Primes help with modulo

## Types

### Linear probing hashing
?
- Can just take current and add P(i)  % size
	- p() is probing function, i is from 1 to size

#### Process
- %10
	- 10-60% full ~ O(1)
	- 60-80% full ~~ O(1)
	- >80% full ~ O(n)

- %11
	- up to 90% ~O(1)

#### Drawback
?
- Clustering


### Quadratic probing
?
- Can just take current and add P(i^2)  % size
	- p() is probing function, i is from 1 to size
- Example probings
	- [![Image from Gyazo](https://i.gyazo.com/c80d4ab4ca44f4c501a315d8f19d674f.png)](https://gyazo.com/c80d4ab4ca44f4c501a315d8f19d674f)

#### Methods
?
- Constant adding
	- [![Image from Gyazo](https://i.gyazo.com/bc7670f48151251046a72ec342fc461d.png)](https://gyazo.com/bc7670f48151251046a72ec342fc461d)
	- Synonyms will produce same sequence, not enter new ones
- Alternating between add and minus
	- [![Image from Gyazo](https://i.gyazo.com/3a1131ab17c8b024ba47bc1136c9c0f8.png)](https://gyazo.com/3a1131ab17c8b024ba47bc1136c9c0f8)
	- Eventually lead to filling

#### Pros/Cons
?
- Pros
	- Reduce primary clustering from linear probing
- Cons
	- Produces different kind of clustering where some are avoided
		- Solution? Have a different hash index sequence for each index

### Random probing
?
- Random number generator
- Probing example
	- [![Image from Gyazo](https://i.gyazo.com/0381d926802fe3767a12523642035f57.png)](https://gyazo.com/0381d926802fe3767a12523642035f57)

### Rehashing
?
- p(i) is a hashing function itself
	- $h_p(k)$ != 0
- Probing sequence
	- [![Image from Gyazo](https://i.gyazo.com/9c3ddb035acb85133db57455e28f87ea.png)](https://gyazo.com/9c3ddb035acb85133db57455e28f87ea)
### Tweak hash table size
?
- Estimate capacity required
- Double it and use as size

References:

Created:: 2022-03-25 18:31
