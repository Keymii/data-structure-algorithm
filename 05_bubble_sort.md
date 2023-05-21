# Sorting Algorithms

## *Bubble Sort*

Bubble sort works on the repeatedly swapping of adjacent elements until they are not in the intended order. It is called bubble sort because the movement of array elements is just like the movement of air bubbles in the water. Bubbles in water rise up to the surface; similarly, the array elements in bubble sort move to the end in each iteration.

Below is the C++ code for the Bubble Sort Algorithm operating on array *arr[]* of length *n*.

```
void bubbleSort(int arr[], int n){
    int i, j;
    for (i = 0; i < n - 1; i++)
        // Last i elements are already in place
        for (j = 0; j < n - i - 1; j++)
            if (arr[j] > arr[j + 1])
                swap(arr[j], arr[j + 1]);
}
```
Time Complexity: $O(n^2)$

Auxiliary Space: $O(1)$ 

The assumed *swap* function in the algorithm will swap the values of given array elements.

The above function runs in $O(n^2)$ even if array is sorted.

## *Optimized Bubble Sort*

```
void bubbleSort(int arr[], int n){
   int i, j;
   bool swapped;
   for (i = 0; i < n-1; i++)
   {
     swapped = false;
     for (j = 0; j < n-i-1; j++)
     {
        if (arr[j] > arr[j+1])
        {
           swap(arr[j], arr[j+1]);
           swapped = true;
        }
     }
 
     // IF no two elements were swapped by inner loop, then break
     if (swapped == false)
        break;
   }
}
```
Time Complexity: $O(n^2)$

Auxiliary Space: $O(1)$ 

But in its best case (ie, sorted array), it runs at $O(n)$. 


-----
[< Previous](./04_selection_sort.md)  &ensp;  [Next >](./06_insertion_sort.md)

[Open Table of Content](./00_table_of_content.md) 

-----