---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, January 20th 2023, 9:20:25 pm
---

# Merge Sort

## Merge

The merge operation is merge sort’s fundamental operation.

- input: two sorted lists
- output: sorted union of the input lists

The steps of this algorithm are:

1. Place pointers at the start of both lists
2. Compare the values at both pointers
3. Insert the smaller value and increment its pointer if possible
4. Repeat steps 2–4 until the ends of both lists are reached

## Base Case

Merge sort’s base case is a singleton list.

A singleton list is considered as sorted.

How to get to the base case?

- top-down
    - break list up until we get down to base case
    - uses a stack
- bottom-up
    - start from single items and join them back together
    - uses a queue

### Top-Down

Steps:

1. Recursively halve list until base case is reached
2. Merge halves back together

### Bottom-Up

Steps:

1. Decompose the list into singletons and enqueue them
2. Merge pairs

## Time and Space Complexities

time complexities for both **top-down** and **bottom-up**: $\Theta(nlogn)$

space complexities:

- top-down
    - array - $\Theta(n)$
    - linked list - $\Theta(logn)$
- bottom-up
    - array - $\Theta(n)$
    - linked list - $\Theta(n)$

## Code

Top down recursive implementation:

```C
mergesort(A, first, last) {
    if (first < last) {
        int i;
        item B[], C[];
        int mid = (last - first + 1) / 2;
        for (i = 0; i < mid; i++) B[i] = A[i];
        for (i = mid; i <= last; i++) C[i - mid] = A[i];
        mergesort(B, 0, mid - 1);
        mergesort(C, 0, mid - 1);
        A = merge(B, C);
    }
}
```