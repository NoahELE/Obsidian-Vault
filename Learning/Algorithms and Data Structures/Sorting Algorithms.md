# Sorting Algorithms

## Insertion Sort

**Algorithm**

To sort an array of size n in ascending order:

1. Iterate from arr[1] to arr[n] over the array.
2. Compare the current element (key) to its predecessor.
3. If the key element is smaller than its predecessor, compare it to the elements before. Move the greater elements one position up to make space for the swapped element.

stability: **stable**

time complexity:

- average - $O(n^2)$
- best (The list is already sorted) - $\Theta(n)$
- worst - $\Theta(n^2)$

## Selection Sort

The selection sort algorithm sorts an array by repeatedly finding the minimum element (considering ascending order) from unsorted part and putting it at the beginning. The algorithm maintains two subarrays in a given array.

stability: **unstable**

time complexity:

- average - $\Theta(n^2)$
- best - $\Theta(n^2)$
- worst - $\Theta(n^2)$

## Quick Sort

Quick Sort is a [Divide and Conquer](https://www.geeksforgeeks.org/divide-and-conquer-introduction/) algorithm. It picks an element as pivot and partitions the given array around the picked pivot. There are many different versions of quick sort that pick pivot in different ways.

1. Always pick first element as pivot.
2. Always pick last element as pivot (implemented below)
3. Pick a random element as pivot.
4. Pick median as pivot.

The key process in quick sort is partition(). Target of partitions is, given an array and an element x of array as pivot, put x at its correct position in sorted array and put all smaller elements (smaller than x) before x, and put all greater elements (greater than x) after x. All this should be done in linear time.

stability: **unstable**

time complexity:

n-element partitions take $\Theta(n)$ time to process.

- average - $O(nlogn)$
- best (balanced) - $O(nlogn)$
- worst (unbalanced) - $O(n^2)$

## Merge Sort

Like [Quick Sort](https://www.geeksforgeeks.org/quick-sort/), Merge Sort is a [Divide and Conquer](https://www.geeksforgeeks.org/divide-and-conquer-introduction/) algorithm. It divides the input array into two halves, calls itself for the two halves, and then merges the two sorted halves. **The merge() function** is used for merging two halves. The merge(arr, l, m, r) is a key process that assumes that arr[l..m] and arr[m+1..r] are sorted and merges the two sorted sub-arrays into one

stability: **stable**

time complexity:

- average - $\Theta(nlogn)$
- best - $\Theta(nlogn)$
- worst - $\Theta(nlogn)$

extra space:
- top-down
    - array - $\Theta(n)$
    - linked list - $\Theta(logn)$
- bottom-up
    - array - $\Theta(n)$
    - linked list - $\Theta(n)$
