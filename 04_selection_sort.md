# Sorting Algorithms

Array sorting is one of the most famous problems in the field of computer programming.

## *Selection sort*

As the name suggests, in selection sorting method, we select the minimum element of the array. Then this element is swapped with the first element. After swapping, we consider the sub-array without the first element and repeat the same.

Let there be an unsorted array *arr[]* with length *n*
```
Algorithm selectionSort(int arr[], int n){
    int i, j, min_idx;
 
    // One by one move boundary of unsorted subarray
    for (i = 0; i < n - 1; i++) {
 
        // Find the minimum element in unsorted array
        min_idx = i;
        for (j = i + 1; j < n; j++) {
            if (arr[j] < arr[min_idx])
                min_idx = j;
        }
 
        // Swap the found minimum element with the first element
        if (min_idx != i)
            swap(arr[min_idx], arr[i]);
    }
}
```
Time complexity : $O(n^2)$

Space complexity :  $O(1)$ (as the only extra memory used is for temporary variables while swapping two values in Array.)

### *Important Note:*
- Selection sort has a time complexity of $O(n^2)$ in the worst and average case. Hence it does not work well on large datasets.
- The selection sort never makes more than $O(n)$ swaps and can be useful when memory writing is costly. 
-----
[< Previous](./03_time_space_complexity.md)  &ensp;  [Next >](./05_bubble_sort.md)

[Open Table of Content](./00_table_of_content.md) 

-----