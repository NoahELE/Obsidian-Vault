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

### Connected Undirected graph

Every pair of vertices is connected (possibly indirectly)

### Unconnected Undirected graph

has unconnected components

## Directed graph

- Edge direction is specified
- Links are not symmetrical

### Weakly Connected Directed Graph

Replace all directed edges with undirected edges, to obtain a connected (undirected) graph

### Strongly Connected Directed Graph

If *every vertex* is **reachable** from *every other vertex*

## Bipartite Graph

- U and V are disjoint sets of vertexes
- Every vertex in U connects to a vertex in V, and vice versa

## Complete graph

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

work on graphs that are:

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
            2. Push its unvisited neighbours into the stack

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
            1. Mark its unvisited neighbours as visited
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

time complexity: $O((V + E)logV)$

### Floyd-Warshall Algorithm

```C
for i
    for j
        for k
            ...
```