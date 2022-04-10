# CMPT225 Question 2
## a
The total time required to push n elements to the stack will be O(n).
For each insertion, the program simply adds to the tail, which is an O(1) operation, n times, as there are n elements to push into the stack. As a result, the operation will take O(n) * O(1) which can be simplified to O(1).

  
## b
To pop those n elements from the stack will take O($n^2$).
In a pop operation, it will take O(n) for the while loop to find the predecessor of the current tail, as it will have to traverse until the `elemCount - 1`th node. Since the loop happens for every pop and there are n pops, the final running time is O(n) * O(n) = O($n^2$)
___
References:

Created:: 2022-02-17 17:51
