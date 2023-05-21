# Sorting Algorithms

## *Insertion Sort*
Pseudocode for insertion sort:
```
Algorithm insertionSort(arr):
    for i = 1 to n-1
        key = arr[i]
        j = i-1
        while j >= 0 and arr[j] > key
            swap arr[j+1] with arr[j]
            j = j - 1
        end while
    end for
end function
```
This algorithm sorts an array of items by repeatedly taking an element from the unsorted portion of the array and inserting it into its correct position in the sorted portion of the array.

1. The procedure takes a single argument, ‘A’, which is a list of sortable items.
The variable ‘n’ is assigned the length of the array A.
2. The outer for loop starts at index ‘1’ and runs for ‘n-1’ iterations, where ‘n’ is the length of the array.
3. The inner while loop starts at the current index i of the outer for loop and compares each element to its left neighbor. If an element is smaller than its left neighbor, the elements are swapped.
4. The inner while loop continues to move an element to the left as long as it is smaller than the element to its left.
5. Once the inner while loop is finished, the element at the current index is in its correct position in the sorted portion of the array.
6. The outer for loop continues iterating through the array until all elements are in their correct positions and the array is fully sorted.

Below is the C++ implementation of the Insertion Sort algorithm:
```
void insertionSort(int arr[], int n){
    int i, key, j;
    for (i = 1; i < n; i++)
    {
        key = arr[i];
        j = i - 1;
 
        // Move elements of arr[0..i-1], 
        // that are greater than key, to one
        // position ahead of their
        // current position
        while (j >= 0 && arr[j] > key)
        {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
```
Time Complexity: $O(n^2)$

Auxiliary Space: $O(1)$ 


-----
[< Previous](./05_bubble_sort.md)  &ensp;  [Next >](./07_quick_sort.md)

[Open Table of Content](./00_table_of_content.md) 

-----