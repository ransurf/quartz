---
title: CMPT 125 Assignments
---
Status: 
Tags: 
Links: [notes/) CMPT 125 - Introduction to Computing Science and Programming II](None)
___
# CMPT 125 Assignments
## Ass 5
- [~ Travelling Salesperson Problem](None)
## Ass 4
- Use isdigit() to tell whether it is an operation or a digit
- is it pre-order if I check the root before parents?
- if its a leaf then its a number
- if its a middle node then it has to be a 

So I went with an alternate method when recursively calling left and right, check if they're a leaf node, if they're not then they need to be wrapped in parentheses, after wrapping the two operands in parentheses (as appropriate), return,with the operator in the middle. And this method works.
### Process
if leaf
	return num
`( `

` )`
## Ass 2
- [HW2-CMPT125-FALL2021.pdf](None)
- 1,2,4,6,7,8,9
### Psuedo-Code
- Adding file
- For each line, if title != title, then add new song at end of file and return 0
	- While loop to check each line, boolean to store whether it is there
### Q1
Extra test cases
- 
### Q2
### Q3
### Q4

```c
#include <stdio.h>
#include <stdlib.h>
#include <stdbool.h>
#include <string.h>
#include <stdbool.h>

#include "assignment2.h"

int add_song(const char* file_name, song s) {

  FILE *fptr = fopen("./songs.db","a");

  if(fptr == NULL) {
    exit(1);             
  }

  if (find_song(file_name, s.title)) {
    return 0;
  } else {
    fwrite(&s, sizeof(s), 1, fptr);
  }

  fclose(fptr);
  return 1;
}



song* find_song(const char* file_name, const char* title) {
  
  FILE *fptr = fopen("./songs.db","r");
  song* s = (song*) malloc(sizeof(song));

  if(fptr == NULL) {
    exit(1);             
  }
  
  while (true) {
    fread(s, sizeof(*s), 1, fptr);
    if (feof(fptr)) {
      break;
    }
   
    if (strcmp(s->title, title) == 0) {
      return s;
    }
  }

  fclose(fptr);
  return NULL;

}


unsigned long fib3(unsigned int n) {
  long* arrFib = (long*) malloc( (n+1) * sizeof(long));

  if (arrFib == NULL)
    return -1; 

  //set first 3 numbers of array to be used in loop
  arrFib[0] = 0; 
  arrFib[1] = 1;
  arrFib[2] = 2;

  //iteratively calculates each number
  for (int i = 3; i<=n; i++) { 
    arrFib[i] = arrFib[i-1] + arrFib[i-2] + arrFib[i-3];
  }

  return arrFib[n];
}


int linear_search_rec_first(int* ar, int length, int number) {
  
  static bool newArray = false;
  static int index = 0;
  
  if (newArray) {
    index = 0;
    newArray = false;
  }
  

  //out of bounds
  if (index >= length) {
    newArray = true;
    return -1;
  }
  printf("index and num: %d %d\n", index, ar[index]);
  if (ar[index] == number) {
    printf("in\n");
    newArray = true;
    return index;
  }

  //increments after each iteration like a for loop
  index++;
  newArray = false;
  return linear_search_rec_first(ar, length, number);
}

int linear_search_rec_last(int* ar, int length, int number) {
  length = length-1;
  
  if (length < 0) {
    return -1;
  }
  if (ar[length] == number) {
    return length;
  }
  
  return linear_search_rec_last(ar, length, number);
}


int count_tokens(const char* str, char delim) {
  // implement me
  int i = 0;
  int numTokens = 0;
  
  while (str[i] != '\0') {
    //adds token count for when non-delim char follows delim
    if ( str[i] == delim && str[i+1] != '\0' && str[i+1] != delim ) {
      numTokens++;
    }
    i++;
  }
  return numTokens; //crashes before returning
}


char** get_tokens(const char* str, char delim) {

  int numTokens = count_tokens(str, delim);
  int currTokenNum = 0;

  char** tokens = malloc(numTokens * sizeof(char*));
  for (int i = 0; i < numTokens; i++)
    tokens[i] = malloc((strlen(str)) * sizeof(char));

  for (int str_i = 0; str_i<strlen(str); str_i++) {
    if (str[str_i] != delim) {
      // char* currTokenPtr = &tokens[currTokenNum];
      int tok_i = 0;
      while (str[str_i] != delim) {
        tokens[currTokenNum][tok_i] = str[str_i];
        str_i++;
        tok_i++;
      }

      printf("\nDONE: tokens[%d] = %s\n\n", currTokenNum, tokens[currTokenNum]);
      currTokenNum++;
    }
  }

  for (int i = 0; i < numTokens; i++) {
    printf("tokens[%d] = %s\n", i, tokens[i]);
  }
  return tokens;
}

//have placeholder string, use val of j to properly alloc mem for string
```
## Reflections
### 1 (86%, -0.7%)
- 4
	- 17
		- max was first value (-12)
		- Didn't apply abs to first value bruh
	- 19
		- max was first value (-1)
		- ^
	- 22
		- Test case was 1, so it would return nothing
## Rules
- Don't print anything, don't run with math.h or modify makefile
- Main will call `assignment`
- Compile using makefile (gcc into machine code)
	- type `make` in console
- Runs on linux, make sure code compiles by running test 1

- maybe have a while loop where the value is changed to the next one in case something happens you know
```
typedef enum {false, true} bool;

  

void str_subtract_one(char* num) {

int strLen = strlen(num);

bool isZeroCase = false; //keeps track on whether to continue

for (int i=strLen-1; i>=0; i--) { //reverse iteration through string

printf("i = %d\n", i);

if (isZeroCase) { //if

printf("nums[i] = %d\n", num[i]);

if (num[i] == '0') {

printf("0 case");

num[i] = '9';

isZeroCase = true; //causes next to update

} else {

num[i] = num[i]-1;

break;

}

}

printf("num is currently: %s\n", num);

}

}
```

for loop, continues to decrease string as `isZero` is true
while currDigit = 0??
___
# Backlinks
```dataview
list from [CMPT 125 Assignments](out/cmpt-125-assignments.md) AND !outgoing([CMPT 125 Assignments](out/cmpt-125-assignments.md))
```
___
References:

Created:: 2021-09-20 14:57