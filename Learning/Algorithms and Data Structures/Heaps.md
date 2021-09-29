# Heaps

## Queues

Implementations:

- Dynamic Array
  - delete min/max - $\Theta(n)$
  - enqueue - $O(n)$ *(might require a realloc)*
- Linked List
  - delete min/max - $\Theta(n)$
  - enqueue - $O(1)$

## Heaps

DownHeap - $O(logn)$

- used in deletion of an element

UpHeap - $O(logn)$

- used in insertion of an element

Bottom-up Heap Construction - $\Theta(n)$

## Heap Sort

1. make heap - $\Theta(n)$
2. delete max element (downheap) - $O(logn)$
3. n deletions

Total time complexity $O(nlogn)$

