---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, January 20th 2023, 9:20:31 pm
---

# Queues

Insert at tail (newest) and remove from head (oldest)

- Abstract data structure
- Dequeue - Take the first item from the head
- Enqueue - Add an item to the tail

Implementation:

- Dynamic Array
    - Move each item up whenever we remove something from queue
    - Dequeue - $\Theta(n)$
    - Enqueue: $O(n)$ – usually $O(1)$
- Linked List
    - Dequeue: $O(1)$ – Prepend insert
    - Enqueue: $O(1)$ – If we keep a pointer to the end of list
- Circular Arrays
    - Keep track of start and end indices
    - Delete at start index and move start along
    - Insert at end index and increment by one,
    - then get remainder from dividing by array size
    - Dequeue: $O(1)$
    - Enqueue: $O(n)$
