---
title: C Strings
---
Status: 
Tags: 
Links: [C Variables](out/c-variables.md)
___
# C Strings
## Principles
- Array of chars
	- 0 is at the end of every array (`\0`)
		- Other elements will not be counted
		- The length of the array can be longer than strlen()
- C stores duplicate strings in the same place
	- `world` from str1 =  `hello world` would have the same adress as str2 = `world`
`<string.h>` for string functions
## Functions
```
strlen() //calculates length of given string
strcmp()
```
### strcpy()
`char * strcpy(char * dest, consnt char * src)`
-   Copies the string src into dest
-   Returns the pointer to the dest
-   What are our requirements about the parameters?
    -   The length of dest must be sufficient to copy src.
```c
char* str_cpy (char* dest, const char* src) {
    int i = 0;
    while (src[i] != '\0') {
        dest[i] = src[i];
        i++;
    }

    dest[i] = 0;
    return dest;
}

```
### strcat()

-   Concatenates 2 strings
-   Appends src to the end of dest

```c
char* strcat (char* dest, const char* src) {
    int i = 0;
    while (dest[i] != '\0') {
        i++;
    } // compute strlen(dest)
    str_cpy(dest+i, src);
    return dest;
}
```
## Syntax
```c
#include <string.h> //includes functions


// Declarations

char* word1 = “Hello”; 
char word2[6] = {‘H’, ‘e’, ‘l’, ‘l’, ‘o’, ‘\0’};

// Printing

char c1 = 'A'; printf("c1 = %c", c1); << A printf("c1 = %d", c1); << 65
	
// Char arithmetic

char ch = 'a'; ch = ch + 3; // sets char = 'd' 
char c = 65; printf("c = %c", c) << A
```
___
# Backlinks
```dataview
list from [C Strings](out/c-strings.md) AND !outgoing([C Strings](out/c-strings.md))
```
#### Array of strings

```c
const char * colors[] = {"Red", "Blue", "Green"}; // array of char*
```

Only the pointers are in the same array, but not the actual data.
___
References:

Created:: 2021-09-15 15:16
