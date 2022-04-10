---
title: MATH232 Computing Assignment 1
---
Status: 
Tags: 
Links: [MatLab](out/matlab.md)
___
# MATH232 Computing Assignment 1
## Finding Answers
### 1
We can find basis by
- Row echelon form
- finding vectors with leading 1
- [Source](https://www.youtube.com/watch?v=0utd-Noc_Fs&ab_channel=patrickJMT)
### 2
W_1= [1 5 2 -1 -1 3; 0 4 1 1 1 1; -1 1 0 2 2 -1; 2 11 3 1 4 2; 1 3 -1 1 1 0; 1 7 2 1 3 1]
W_2= [5 2 1 2 0 2; 2 -1 2 -4 1 0; 1 0 1 -2 2 -2; 7 0 1 4 3 3; 1 1 0 1 -1 1; 5 2 1 2 1 1]
[Calculating span of matrix in matlab](https://math.stackexchange.com/questions/1406027/calculating-the-span-of-a-matrix-in-matlab)
## Report
### Part 1
>> R=rand(5,7)

R =

    0.8147    0.0975    0.1576    0.1419    0.6557    0.7577    0.7060
    0.9058    0.2785    0.9706    0.4218    0.0357    0.7431    0.0318
    0.1270    0.5469    0.9572    0.9157    0.8491    0.3922    0.2769
    0.9134    0.9575    0.4854    0.7922    0.9340    0.6555    0.0462
    0.6324    0.9649    0.8003    0.9595    0.6787    0.1712    0.0971

>> rref(R)

ans =

    1.0000         0         0         0         0   -0.8409    1.9764
         0    1.0000         0         0         0    3.7698   -5.9264
         0         0    1.0000         0         0    3.8571   -4.0608
         0         0         0    1.0000         0   -8.0047    9.2175
         0         0         0         0    1.0000    2.4444   -1.5157

A matrix's rows are not linearly independent if there is a zero row vector, as that would imply that one of the vectors were a linear combination of other ones. 
The MATLAB output produced implies that the rows are linearly independent since there are no non-vectors.

However, the columns are not linearly independent because there are more columnns then there are rows, meaning that there will be at least one columnar vector that can be expressed as the linear combination of other vectors.
1.  but not every column has a pivot point so the column vectors are dependent

[![Image from Gyazo](https://i.gyazo.com/d5c94b30f5c1eddd71d36dd78d1babb1.png)](https://gyazo.com/d5c94b30f5c1eddd71d36dd78d1babb1)

The bases for col(R) are the columnar vectors that contain leading 1's in RREF. In this case, it would be the first 5 columns of R, as they all contain leading 1's. Since there are 5 vectors, there are 5 dimensions.
### Part 2
- Show reduced
- Both W1 and W2 are 4 dimensions since there are both have a rank of 4.
- Basis can be found by finding the original column vectors in the positions of the leading 1's
- for v1 that would be cols 1,2,3,4
	- basis would be:
		- [1 0 -1 2 1 1; 5 4 1 11 3 7; 2 1 0 3 -1 2; -1 1 2 1 1 1]
		- [1 5 2 -1; 0 4 1 1; -1 1 0 2; 2 11 3 1; 1 3 -1 1; 1 7 2 1]
- for v2 that would be cols 1,2,3,5
	- basis would be:
		- [5 2 1 2 0 2; 2 -1 2 -4 1 0; 1 0 1 -2 2 -2; 1 1 0 1 -1 1]
		- [5 2 1 0; 2 -1 2 1; 1 0 1 2; 7 0 1 3; 1 1 0 -1; 5 2 1 1]
- Find intersection by cat(2,W_1,W_2)

W_3 = cat(2, W_1_B, -W_2_B)
rref(W_3)
#### Procedure
W_1= [1 5 2 -1 -1 3; 0 4 1 1 1 1; -1 1 0 2 2 -1; 2 11 3 1 4 2; 1 3 -1 1 1 0; 1 7 2 1 3 1]
W_1 = rref(W_1)
W_2= [5 2 1 2 0 2; 2 -1 2 -4 1 0; 1 0 1 -2 2 -2; 7 0 1 4 3 3; 1 1 0 1 -1 1; 5 2 1 2 1 1]
W_2 = rref(W_2)
B1 = [1 5 2 -1; 0 4 1 1; -1 1 0 2; 2 11 3 1; 1 3 -1 1; 1 7 2 1]
B2 = [5 2 1 0; 2 -1 2 1; 1 0 1 2; 7 0 1 3; 1 1 0 -1; 5 2 1 1]
W_3 = cat(2, B1, -B2)
W_3 = rref(W_3)
___
# Backlinks
```dataview
list from [MATH232 Computing Assignment 1](out/math232-computing-assignment-1.md) AND !outgoing([MATH232 Computing Assignment 1](out/math232-computing-assignment-1.md))
```
___
References:

Created:: 2022-01-19 22:42
