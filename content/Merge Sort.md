Status: 
Tags: #archivedCards/cmpt125/algorithms
Links: [[Sorting Algorithms]]
___
# Merge Sort
## Principles

Keeps relative sort order, as it wouldnt swap same elements

For disk-bound data
?
- Good for disk-bound data as you don't have to always have access to the whole array, as it is just comparing adjacent/small chunks
	- Fetch information in blocks so its supported

Stages
- Partition
	- Sort the two halves then merge into new array
- Sorting
	- Requires more memory to create new array

Worst, average, best case in bigO ;; Always O(nlogn)
<!--SR:!2021-12-17,2,175-->

Space complexity
?
- O(n)

Prove running time
?
T(N) = 2 x T(n/2) + 3n
= 2 x (2 x T(N/4) + (3N/2)) + 3N
= 4 x T(N/4) + 2 x (3N/2) + 3N
- Stopping condition is N x T(N/N) + (3N + ... + 3N)
= N x T(1) + 3N x log2(N) %%N/N simplified, no clue what's next bruh%%
= O(NlogN) %%simplified into the second part, NlogN%%
<!--SR:!2021-12-21,8,210-->

## Implementation
?
```c
void merge(int A[], int mid, int n) {

  int* tmp = (int*) malloc(n*sizeof(int));

  int i = 0;
  int j = mid;
  int k = 0;

  while (k<n) {

    if (i==mid || (j<n && A[j] < A[i])) {
      tmp[k] = A[j];
      j++;
    } else {
      tmp[k] = A[i];
      i++;
    }
    k++;
  }

  for(int k = 0; k < n; k++)
      A[k] = tmp[k];  

  free(tmp);

}
void mergeSort(int arr[], int r) {
  
  if (r >= 2) { //goes until size 0 arr
    int m = r/2;

    mergeSort(arr, m);
    mergeSort(arr+m, r-m);

    merge(arr, m, r);
  }

}
```
___
# Backlinks
```dataview
list from [[Merge Sort]] AND !outgoing([[Merge Sort]])
```
___
References:
<!--SR:!2021-12-16,1,130-->

Created:: 2021-10-04 15:51
