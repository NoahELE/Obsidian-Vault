---
date created: Tuesday, January 4th 2022, 10:53:47 am
date modified: Friday, January 20th 2023, 9:20:34 pm
---

# Graph

Graph:

- a representation of a set of objects
- some pairs of objects are connected by links

properties:

- vertices
- edges
- directedness
- cyclicity
- connectivity
- weightedness

can be represented by:

- adjacency matrix
- adjacency list

Graph G = {V,E} Set of:

- Vertices V: can contain information
- Edges E (links between vertices): can have direction and/or weight

Compared to trees and linked lists:

- vertices = nodes
- edges = links

## Undirected Graph

Edges have no direction specified

### Connected Undirected Graph

Every pair of vertices is connected (possibly indirectly)

### Unconnected Undirected Graph

has unconnected components

## Directed Graph

- Edge direction is specified
- Links are not symmetrical

### Weakly Connected Directed Graph

Replace all directed edges with undirected edges, to obtain a connected (undirected) graph

### Strongly Connected Directed Graph

If _every vertex_ is **reachable** from _every other vertex_

## Bipartite Graph

- U and V are disjoint sets of vertexes
- Every vertex in U connects to a vertex in V, and vice versa

## Complete Graph

all vertices is directly connected to all other vertices

$E = V(V-1)$ E is the number of edges and V is the number of vertices

## Graph Representation

### Matrix

**undirected graph**:

| \   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 1   | 1   |
| 2   | 1   | 1   | 0   | 1   |
| 3   | 0   | 1   | 1   | 0   |

**weighted undirected graph**:

| \   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 20  | 5   | 0   |
| 1   | 20  | 0   | 30  | 1   |
| 2   | 5   | 30  | 0   | 45  |
| 3   | 0   | 1   | 45  | 0   |

**directed graph**:

| \   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 1   | 1   | 0   |
| 1   | 1   | 0   | 0   | 1   |
| 0   | 0   | 1   | 0   | 1   |
| 0   | 0   | 1   | 0   | 0   |
|     |     |     |     |     |

**weighted directed graph**:

| \   | 0   | 1   | 2   | 3   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 20  | 3   | 0   |
| 1   | 2   | 0   | 32  | 1   |
| 20  | 5   | 30  | 0   | 4   |
| 12  | 0   | 1   | 45  | 0   |

complexity:

- space: $\Theta(|V|^2)$
- retrieve edge: $O(1)$

### List

complexity:

- space: $\Theta(|V| + |E|)$
- retrieve edge: $O(deg(V)) = O(V)$

## Search Algorithms

### Depth-First Search

find a path between two vertices and it's _guaranteed_ to do so.

may not be the shortest path

works on graphs that are:

- connected
- unweighted
- directed

The steps of this algorithm are:

1. Push the source vertex into the stack
2. While the stack is not empty:
   1. Pop a vertex from the stack
   2. If said vertex is:
      1. the destination: stop
      2. visited: continue
      3. unvisited:
         1. Mark it as visited
         2. Push its unvisited neighbors into the stack

### Breadth-First Search

_guaranteed_ to find the shortest path

works on graphs that are:

- connected
- unweighted
- directed
- cyclic

The steps of this algorithm are:

1. Enqueue the source vertex into the queue
2. Mark said vertex as visited
3. While the queue is not empty:
   1. Dequeue a vertex from the queue
   2. If said vertex is:
      1. the destination: stop
      2. otherwise:
         1. Mark its unvisited neighbors as visited
         2. Enqueue said neighbours into the queue

### Uniform Cost Search

an _adaptation_ of breadth-first search to make it work on weighted graph

works on graphs that are:

- connected
- weighted: no negative edges
- directed
- cyclic

### Dijkstra’s Algorithm

find the shortest path from a vertex to every other vertex

data structures used are:

- priority queue of vertices
- list of shortest distance and preceding vertices in shortest path

time complexity: $O((V + E)logV)$ (using heap as priority queue)

- deletemin - $O(logV)$
- update - $O(logV)$
- deletemin - $O(V)$ times
- update - $O(E)$ times

time complexity: $O(E + VlogV)$ (using a Fibonacci heap)

- deletemin - $O(logV)$
- update - $O(1)$
- deletemin - $O(V)$ times
- update - $O(E)$ times

### Floyd-Warshall Algorithm

All pairs shortest path algorithm

If the graph is sparse, we can say $E = V$, in this case, running Dijkstra for all vertices is a good choice.

If the graph is dense, we can say $E = V^2$, in this case, Floyd-Warshall is better.

weighted directed graphs (weight can be negative)

```C
/*
A[i][i] = 0, no path = INT_MAX
i for intermediate
s for source
t for traget
*/
for (i = 0; i < V; i++) {
    for (s = 0; s < V; s++) {
        for (t = 0; t < V; t++) {
            if (A[s][i] + A[i][t] < A[s][t])
                A[s][t] = A[s][i] + A[i][t];
        }
    }
}
```

data structures used: 2 matrices

- 1 for shortest distance and
- 1 for previous vertex

time complexity: $\Theta(V^3)$

- for dense graph $\Theta(E^{3/2})$
- for sparse graph $\Theta(E^3)$
