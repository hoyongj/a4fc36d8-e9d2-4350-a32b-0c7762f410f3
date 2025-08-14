You’re right—I’ll restart and cover **all** the uploaded CMPT 225 lecture notes, minimizing overlap and focusing on **key terminology** in clean Markdown. Here’s a compact, exam-ready glossary organized by topic (spanning Weeks 3–13).

---

# lists (wk3)

* **node** — object storing an element and link(s).
* **head / tail** — first / last real node.
* **singly linked list** — `next` only; O(1) add/remove at head, linear search.
* **doubly linked list** — `prev` & `next`; O(1) add/remove at both ends.
* **circular list** — tail->next points to head.
* **sentinel (header/trailer)** — dummy boundary nodes that simplify edge cases.
* **link hopping / traversal** — walking node-to-node.
* **Big Three** — destructor, copy ctor, assignment operator for owning structures.

---

# stacks (wk4)

* **stack (LIFO/FILO)** — ADT with `push`, `pop`, `top`, `size`, `isEmpty`.
* **array‑based stack** — fixed cap; `top` index; all ops amortized/constant time.
* **list‑based stack** — uses list; unlimited growth; O(1) `push`/`pop` at front.
* **use‑cases** — undo/redo, call stack, balanced parentheses.

---

# queues & deques (wk4–5)

* **queue (FIFO)** — `enqueue`, `dequeue`, `front`, `size`, `isEmpty`.
* **circular array queue** — `front`/`rear` indices modulo N (avoids shifting).
* **linked‑list queue** — head=dequeue, tail=enqueue; O(1) both ends.
* **deque** — double‑ended queue: `addFirst`/`addLast`/`removeFirst`/`removeLast`.
* **std::deque** — segmented blocks (map-of-chunks) → amortized O(1) at both ends.
* **adapter pattern** — wrapper to present one interface via another (e.g., stack via deque).

---

# iterators & containers (wk5–6)

* **container** — structure exposing traversal via iterators (`begin()`, `end()`).
* **iterator categories** — input/output, forward, bidirectional, random access.
* **iterator ops** — `*p`, `++p`, `--p`, range `[first, last)`, insert/erase by iterator.

---

# trees: core terms (wk6)

* **tree** — non‑linear structure of **vertices (nodes)** and **edges**.
* **rooted tree** — distinguished **root**; **parent/child/siblings** relations.
* **ancestor/descendant**, **subtree**.
* **depth (level)** — edges from root; **height** — max depth in tree.
* **internal / external (leaf)** nodes.
* **ordered tree** — left‑to‑right order among siblings.
* **complete tree** — all levels full except possibly last, filled left→right.
* **perfect tree** — all levels completely full.
* **balanced tree** — subtrees’ heights close (definition depends on variant).
* **traversals** — preorder, inorder (binary), postorder; breadth‑first (level order).

---

# binary trees & array mapping (wk6–7)

* **binary tree** — ≤2 children per node.
* **array representation** — index i: left=2i, right=2i+1 (index 1 as root).
* **linked representation** — node with `left`, `right`, (and optionally `parent`).
* **inorder traversal (binary)** — left, node, right (sorted order for BST).

---

# binary search tree — bst (wk8)

* **bst property** — left subtree keys < node key < right subtree keys.
* **search / insert** — follow comparisons to external position; insert at blank external.
* **deletion cases** — (1) leaf, (2) one child (bypass), (3) two children → replace with **predecessor** (max of left) or **successor** (min of right), then delete that node.
* **height‑sensitive cost** — O(h), worst‑case O(n) when unbalanced.

---

# priority queues & heaps (wk8)

* **priority queue (min/max)** — remove/peek the min (or max) key.
* **heap (binary, array‑based)** — **complete** binary tree with **heap order**:

  * **min‑heap** parent ≤ children; **max‑heap** parent ≥ children.
  * **up‑heap (bubble‑up)** on insert; **down‑heap (bubble‑down)** on removeMin/Max.
* **complexities** — `insert` O(log n), `removeMin/Max` O(log n), `min/max` O(1).
* **heap sort** — build heap + repeatedly remove; O(n log n), in‑place (array heap).

---

# maps & hash tables (wk8)

* **map (ordered map)** — unique keys → values; operations: `get/put/remove`, `keySet/values/entrySet`.
* **hash table** — stores by **hash(key)**:

  * **collision resolution**: **separate chaining** (bucket lists), **open addressing** (linear/probing/double hashing).
  * **load factor (α)** — n / tableSize; triggers **rehashing** when high.
  * **expected O(1)** for search/insert/delete under good hashing and α control.

---

# skip list (wk9)

* **idea** — layered, probabilistically balanced linked lists to support fast jumps.
* **levels (towers)** — each higher level holds \~half of nodes below (in expectation).
* **search** — scan right while ≤ key, drop down when next exceeds key; average O(log n).
* **insert/delete** — as search + coin‑flip promotions / level removals; average O(log n).
* **space** — \~2n nodes on average (linear).
* **node shapes** — **quad node** (prev/next/above/below) or **tower node** with forward array.

---

# avl tree (wk9–10)

* **avl property** — for every node, |height(left) − height(right)| ≤ 1.
* **balance factor** — height(right) − height(left).
* **rotations** — single (LL/RR) and double (LR/RL) rotations.
* **trinode restructuring** — identify `x, y, z` (child/parent/grandparent) and rotate so the median key becomes new root of the trio.
* **guarantees** — height O(log n); `search/insert/delete` O(log n).

---

# (2,4) tree / 2–4 tree (wk10–11)

* **multi‑way balanced search tree** — nodes hold 1–3 keys, 2–4 children.
* **perfectly balanced** — all leaves at same depth; height O(log n).
* **insert** — add into leaf; on overflow **split** and push middle key up (may cascade).
* **delete** — if underflow: **transfer** from sibling with extra key or **fuse** siblings and pull key down from parent (may cascade).
* **operations** — `search/insert/delete` O(log n).

---

# sorting algorithms (wk11)

* **stability** — preserves relative order of equal keys (true for insertion/merge/radix; false for quick/heap by default).
* **in‑place** — O(1) extra space (true for insertion/quick/heap; false for classic merge).
* **insertion sort** — in‑place, stable; O(n²) worst/avg, O(n) best (nearly sorted).
* **merge sort** — stable; O(n log n) time; O(n) extra space; divide–conquer (split→merge).
* **quick sort** — avg O(n log n), worst O(n²); randomized pivots mitigate worst case; in‑place (partitioning).
* **heap sort** — in‑place O(n log n); not stable.
* **bucket sort** — non‑comparison; distribute into buckets then sort/concatenate; linear in model‑dependent settings.
* **radix sort** — digit‑by‑digit stable passes; O(d(n + K)) for d digits, K alphabet size.
* **C++ `sort` / `stable_sort`** — `sort`: intro‑sort (quick + heap fallback) & insertion for tiny ranges; `stable_sort`: merge‑sort variant.

---

# graphs (wk12)

* **graph G=(V,E)** — vertices and edges.
* **directed / undirected**; **weighted**; **connected / disconnected**.
* **representations**:

  * **edge list** — vectors of vertices & edges; simple but slow adjacencies.
  * **adjacency matrix** — n×n; O(1) adjacency test; O(n²) space.
  * **adjacency list** — per‑vertex neighbor lists; O(n+m) space; fast for sparse graphs.
* **traversals** — **BFS** (layers, shortest paths in unweighted), **DFS** (depth exploration).
* **dijkstra** — single‑source shortest paths with non‑negative weights; PQ‑based; O(m log n) with binary heap.

---

# minimum spanning trees (wk13)

* **spanning tree** — connects all vertices with |V|−1 edges (no cycles).
* **mst** — spanning tree of minimum total weight.
* **cut property** — the lightest edge crossing any cut that respects the partial MST is in every MST.
* **cycle property** — the heaviest edge on any cycle is not in an MST.
* **kruskal’s algorithm** — sort edges by weight, add if they don’t form a cycle; uses **disjoint set / union‑find** with `makeSet`, `find`, `union`.
* **prim‑jarník** — grow a cloud from any start vertex, repeatedly add lightest edge to outside vertex; PQ for frontier edges.
* **complexities** — with heaps & union‑find, O(m log n).

---

# algorithm design & analysis reminders (scattered)

* **asymptotics** — O, Ω, Θ; ignore constants / lower‑order terms for growth class.
* **design paradigms** — recursion (incl. **tail**, **binary**), divide‑and‑conquer, greedy, dynamic programming, amortization, prune‑and‑search, brute force.
* **C++ STL anchors** — `list`, `vector`, `deque`, `queue`, `priority_queue`, `map`, `multimap`.

---

## coverage notes

This glossary aggregates the key terms from the provided Weeks **3–13** slide decks and groups overlapping ideas once (e.g., tree basics used by BST/AVL/(2,4), priority queues used by heaps, etc.), so you don’t have to reread duplicates.

If you want, I can now generate a **one‑page cram sheet** (super‑tight bullets + tiny examples) or a **checklist quiz** for self‑testing each section.
