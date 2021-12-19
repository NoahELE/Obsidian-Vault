# Minimum Spanning Tree

Undirected weighted graphs

Minimum spanning tree = subgraph that is:

- A tree (no cycles)
- Contains every vertex (spans)
- Minimum sum of edge weights

Also called:

- Minimum weight spanning tree (sum of weights )
- Minimal spanning tree (might be more than one)

Graph must be connected

MST must have exactly V‐ 1 edges

No cycles in MST

## Prim's Algorithm

vertex based approach

Almost the same as Dijkstra, but the weight does not accumulate.

Preferred method for **dense** graphs

Easiest with matrix representation

Prim’s algorithm relies on picking the next best edge that joins two set of vertices:

- Vertices already in the tree (S)
- Vertices not yet in the tree (V ‐S)

Pseudo Code:

```C
void prim(G, w, root) {
    for every u in V {
        dist[u] = ∞;
        inmst[u] = FALSE;
    }
    dist[root] = 0;
    pred[root] = NULL;
    PQ = makePQ(V); /* all vertices in PQ */
    while (!empty PQ) {
        u = deletemin(PQ);
        for every (v adjacent to u) {
            if ((inmst[v] == FALSE)&& (w[u][v] < dist[v])) {
                dist[v] = w[u][v]; /* update distance */
                decreasewt(PQ, v, dist[v]);/* update PQ dist*/
                pred[v] = u; /* update path information */
            }
        }
        inmst[u] = TRUE;
    }
} /* at end: MST = {{v,pred[v]}: v in V – {root}} */
```

time complexity: $O((V + E)logV) = O(ElogV)$ (for dense graph with heap PQ)

## Kruskal Algorithm

edge based approach

Prim’s algorithm adds the next closest vertex.

Kruskal’s algorithm adds the next lowest weight edge that doesn’t form a cycle.

Pseudo Code:

```C
E1: edges in MST so far
E2: remaining edges

E1 = EMPTYSET, E2 = E
Sort edges in E2 by weight
while |E1| < |V|-1 edges and E2 not EMPTYSET
    Pick min cost edge e(i,j) from E2
    E2 = E2 \ e(i,j)
    if V(i),V(j) are not in same MST so far, then
        E1 = E1 Union e(i,j)
        unite MSTs with V(i) and V(j)
```

time complexity: $O(ElogE + E + V) = O(ElogE)$
