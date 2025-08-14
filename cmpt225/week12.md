
# CMPT 225 – Week 12: Graphs Definition Summary

## **Graph Basics**

* **Graph**: A pair $(V, E)$ where:

  * $V$ = set of **vertices** (nodes)
  * $E$ = collection of **edges** (pairs of vertices)
* **Directed Edge**: Ordered pair $(u, v)$ with origin $u$ and destination $v$.
* **Undirected Edge**: Unordered pair $(u, v)$.
* **Weighted Graph**: Graph with a numerical value (weight) assigned to each edge.
* **Connected Graph**: Every pair of distinct vertices has a path between them.
* **Disconnected Graph**: At least two vertices have no path connecting them.

---

## **Graph Representations**

### **Edge List**

* Stores a list of vertices and a list of edges.
* **Complexities** (n = |V|, m = |E|):

  * Space: $O(n + m)$
  * Insert Vertex: $O(1)$
  * Insert Edge: $O(1)$
  * Remove Vertex: $O(m)$
  * Remove Edge: $O(1)$
  * Is Adjacent: $O(m)$

### **Adjacency Matrix**

* n × n matrix $A$ where entry $a_{ij}$ indicates presence/weight of edge from $i$ to $j$.
* **Complexities**:

  * Space: $O(n^2)$
  * Insert Vertex: $O(n^2)$
  * Insert Edge: $O(1)$
  * Remove Vertex: $O(n^2)$
  * Remove Edge: $O(1)$
  * Is Adjacent: $O(1)$

### **Adjacency List**

* Each vertex has a list of adjacent vertices.
* **Complexities**:

  * Space: $O(n + m)$
  * Insert Vertex: $O(1)$
  * Insert Edge: $O(1)$
  * Remove Vertex: $O(\text{deg}(v))$
  * Remove Edge: $O(1)$
  * Is Adjacent: $O(\text{deg}(v))$

---

## **Graph Traversal**

### **Depth-First Search (DFS)**

* Explores as far as possible along each branch before backtracking.
* Can be implemented recursively or using a stack.
* **Time Complexity**: $O(n + m)$
* Applications:

  * Find a path between two vertices
  * Detect cycles

### **Breadth-First Search (BFS)**

* Explores neighbors level by level, using a queue.
* **Time Complexity**: $O(n + m)$
* Applications:

  * Find shortest path in terms of number of edges
  * Detect cycles

---

## **Weighted Graph Shortest Paths**

### **Dijkstra’s Algorithm**

* Finds shortest paths from a single source in weighted graphs with **nonnegative weights**.
* Uses a priority queue to select the next closest vertex.
* **Complexity**:

  * Removing all vertices from PQ: $O(n \log n)$
  * Relaxing all edges: $O(m \log n)$
  * Connected graph: $O(m \log n)$

