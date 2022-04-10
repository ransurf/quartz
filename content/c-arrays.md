---
title: C Arrays
---
Status: 
Tags: 
Links: [C Variables](out/c-variables.md)
___
# C Arrays
- **constant** variable, fixed length
- Treated as pointers
	- Memory location is not needed to be known
- Variable of an int array is just an int pointer
- Each element in an array is stored in a continuous block, starting from array pos
- Jump in adress when iterating depends on the var type stored in the arr
- `array[i]` == `*(array+i)` where `i` is index
- Array parameters should be `const`
	- `const int ONE = 1;` or `int const ONE = 1;
- String arrays hold the pointers for the starts of each string
- Accessing outside bounds
	- Could lead to crash, or access of garbage data

```c
int arr[2] = {0, 1, 2} //stating size isn't necessary

//Changing Values
arr [2] = 3;
(array + 2) = 3; //equivalent

___
# Backlinks
```dataview
list from [C Arrays](out/c-arrays.md) AND !outgoing([C Arrays](out/c-arrays.md))
```
## Examples
###### Average of an array's values
```c
float average(float ar[], int n) {
    float sum = 0; 

    for (int i = 0; i < n; i++) {
        sum += ar[i];
    }

    return sum / n; 
}

int main() {
    float arr[6] = {0.2, 4.5, 1.2, 5.5, 1.1, -1.2};
    float avg = average(arr, 6);
    return 0; 
}
```
###### Copy Array
Write a function that gets arrays of ints of length n and copies all data from one array into the other.

```c
void copy_arry(float* dest, const float* src, int n) {
    for (int i = 0; i < n; i++) {
       dest[i] = src[i];
    }
}

int main() {
    float arr[6] = {0.2, 4.5, 1.2, 5.5, 1.1, -1.2};
    float arr2[6] = {0.2, 4.5, 1.2, 5.5, 1.1, -1.2};

    copy_arry(arr, arr2, 6);
    return 0; 
}
```
## Multidimensional Array

-   So far we've only seen 1D arrays
-   But often we need 2D / 3D arrays
-   Examples:
    -   Picture: Each entry in the array is the color of a pixel (.bmp format)
    -   Temperature at each point in the room

Creating a 2D array

```c
int width = 640, height = 480;
int image[height][width];
```
### Accessing a 2D array
```c
image[i][j] = 128; 
// ---- OR --- 
(*(image + i))[j] = 128 // each element of image is type of int[width] 
// the size of each element is sizeof(int)*width 
```

See `multid_array.c`

Q: Is the type `int**` is equivalent to `int[][]`

A: `int**` is

-   Array of pointers
-   Array of (1D) arrays, possibly different lengths
-   Pointer to a pointer
___
References: [C - Array of pointers (tutorialspoint.com)](https://www.tutorialspoint.com/cprogramming/c_array_of_pointers.htm)

Created:: 2021-09-13 15:35
