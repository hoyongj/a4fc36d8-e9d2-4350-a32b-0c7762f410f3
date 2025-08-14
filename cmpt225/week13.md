# CMPT 225 – Week 13: Minimum Spanning Trees & Sets

## **Spanning Tree**

* A subset of a graph’s edges that connects all vertices **without cycles**.
* Can be produced by BFS or DFS.

## **Minimum Spanning Tree (MST)**

* A spanning tree of a **weighted graph** that has the **minimum total edge weight**.

---

## **Prim–Jarnik’s Algorithm**

* **Purpose**: Finds an MST.
* **Approach**:

  * Start from an arbitrary vertex $s$, grow MST as a “cloud” of vertices.
  * Each vertex $v$ has a label $d(v)$ = smallest weight edge connecting $v$ to the cloud.
  * At each step:

    1. Add vertex outside the cloud with smallest $d(v)$.
    2. Update $d(v)$ for vertices adjacent to the added vertex.
* **Complexity**: $O((n + m) \log n)$ with adjacency list + heap-based priority queue.
* **Similar To**: Dijkstra’s algorithm (but for MST, not shortest paths).

---

## **Kruskal’s Algorithm** (mentioned in comparison)

* Sorts edges by weight, adds edges to MST if they don’t form a cycle.
* Uses **Union–Find** data structure.

---

## **Set (Data Structure)**

* **Definition**: Collection of unique elements, no order implied.
* **Core Operations**:

  * `Add` – Insert an element.
  * `Remove` – Delete an element.
  * `Contains` – Check membership.
  * `Iterator` – Access all elements.

---

## **C++ Implementations**

* `std::set`: Ordered set (red-black tree).
* `std::unordered_set`: Unordered set (hash table).

---

## **Set Theory Operations**

* **Union**: Combines elements from two sets (no duplicates).

  * Example: $\{3,2,6\} \cup \{5,6,9\} = \{3,2,6,5,9\}$
* **Intersection**: Elements common to both sets.

  * Example: $\{3,2,6\} \cap \{5,6,9\} = \{6\}$
* **Subtraction (Difference)**: Elements in one set but not the other.

  * Example: $\{3,2,6\} - \{5,6,9\} = \{3,2\}$

---

## **C++ Set Operations via `<algorithm>`**

* `set_union`
* `set_intersection`
* `set_difference`
* Require **ordered containers** with iterators.
* Since C++17: `.merge()` method for sets.

