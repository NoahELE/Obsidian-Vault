---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, January 20th 2023, 9:20:23 pm
---

# Heaps

## Priority Queues

Implementations:

- Dynamic Array
    - delete min/max - $\Theta(n)$
    - enqueue - $O(n)$ _(might require a realloc)_
- Linked List
    - delete min/max - $\Theta(n)$
    - enqueue - $O(1)$

## Heaps

DownHeap - $O(logn)$

- used in deletion of an element

UpHeap - $O(logn)$

- used in insertion of an element

Bottom-up Heap Construction (also known as heapify, fixheap, makeheap etc.) - $\Theta(n)$

## Heap Sort

1. make heap - $\Theta(n)$
2. delete max element (downheap) - $O(logn)$
3. n deletions

stability: **unstable**

Total time complexity: $O(nlogn)$
