Status: 
Tags: 
Links: [[CMPT 125 Practice Problems]]
___
# CMPT 125 Basics of Coding in C Practice Problems
7
```c
#include <stdio.h>

void print_max_number(const int digits[], int n) {
	
	int digitCount[9] = {0, 0, 0, 0, 0, 0, 0, 0, 0};
	
	for (int i=0; i<n; i++) {
		int digit = digits[i];
		digitCount[digit]++;
	}
	
	for (int i=8; i>=0; i--) {
		while (digitCount[i] > 0) {
			printf("%d", i);
      digitCount[i]--;
		}
	}
	
}

int main() {
	const int arr[5] = {5, 2, 8, 4, 3};
	print_max_number(arr, 5);
	return 0;
}
```

9
```c
#include <stdio.h>
#include <string.h>

void reverse(char str[]) {
  int len = strlen(str);
  for (int i=0;i<len/2;i++) {
    int temp = str[i];
    str[i] = str[len-i-1];
    str[len-i-1] = temp;
  }
}

int main() {
	char string[] = "52843";
	reverse(string);
  printf("%s", string);
	return 0;
}
```

10

___
# Backlinks
```dataview
list from [[CMPT 125 Basics of Coding in C Practice Problems]] AND !outgoing([[CMPT 125 Basics of Coding in C Practice Problems]])
```
___
References:

Created:: 2021-10-23 14:27
