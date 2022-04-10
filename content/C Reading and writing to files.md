Status: 
Tags: 
Links: [[C Reading and writing (stdin, stdout)]]
___
# C Reading and writing to files
```c
//Setting a file path
FILE *fptr;
fptr = fopen("./{filename}","{mode}");
```
fgets reads the file until it either reaches the character limit (specified by the second argument) or reaches a newline character ('\n'). If you don't put newlines when your adding songs to the file it won't know where the lines end.
___
# Backlinks
```dataview
list from [[C Reading and writing to files]] AND !outgoing([[C Reading and writing to files]])
```
___
References:

Created:: 2021-10-05 16:37
