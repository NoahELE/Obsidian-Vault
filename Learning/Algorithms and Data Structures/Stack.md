---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, January 20th 2023, 9:20:19 pm
---

# Stack

- Insert at top (newest)
- Take from top (newest)
- Abstract Data Structure
    - Push – Add an item to the top of the stack
    - Pop – Take an item from the top of the stack

## Implementation

- Linked List
    - Push - $O(1)$ - Prepend
    - Pop - $O(1)$ - `top = top->next`
- Dynamic Array
    - Push - $O(n)$ - $O(n)$ if we have to reallocate
    - Pop - $O(1)$
