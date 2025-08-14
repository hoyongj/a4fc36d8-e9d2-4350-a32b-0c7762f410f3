
# 📚 CMPT 225 – Week 3 Key Definitions

## 1. **Arrays**

* **Array**: An Abstract Data Type (ADT) storing a fixed-size, indexed collection of elements of the same type.
* **Static Array**: Size fixed at compile time.
* **Dynamic Array**: Allocated with `new`; size fixed at allocation time.
* **Characteristics**:

  * Random access (O(1) element access).
  * Size cannot change without creating a new array and copying data.
  * Not objects in C++ (no methods, no bounds checking).
* **Insertion into Array**: Requires shifting elements; O(n).
* **Removal from Array**: Requires shifting elements; O(n).
* **Insertion Sort**: Simple sorting algorithm that builds a sorted array one element at a time.

---

## 2. **Standard Library Array (`std::array`)**

* **Template**: `std::array<T, N>` — fixed-size, object wrapper around a built-in array.
* **Member Function Categories**:

  * **Iterators**: `begin()`, `end()`, `rbegin()`, `rend()`.
  * **Capacity**: `size()`, `max_size()`, `empty()`.
  * **Access**: `operator[]`, `at()`, `front()`, `back()`, `data()`.
  * **Modifiers**: `fill()`, `swap()`.

---

## 3. **Vectors (`std::vector`)**

* **Vector**: Resizable array-like container supporting dynamic growth/shrinkage.
* **Member Function Categories**:

  * **Big Three**: Constructor, Destructor, Assignment Operator.
  * **Iterators**: `begin()`, `end()`, `rbegin()`, `rend()` and constant versions.
  * **Capacity**: `size()`, `max_size()`, `resize()`, `capacity()`, `empty()`, `reserve()`, `shrink_to_fit()`.
  * **Access**: `operator[]`, `at()`, `front()`, `back()`, `data()`.
  * **Modifiers**: `assign()`, `push_back()`, `pop_back()`, `insert()`, `erase()`, `swap()`, `clear()`, `emplace()`, `emplace_back()`.

---

## 4. **2D Arrays**

* **Static 2D Array**: `int arr[rows][cols];`
* **Dynamic 2D Array**: Array of pointers to arrays.
* **`std::vector<std::vector<T>>`**: Dynamic and resizable alternative for 2D data.

---

## 5. **Lists**

* **List**: A sequence of nodes where each node stores:

  * An element (data).
  * One or more links to other nodes.
* **Advantages over Arrays**:

  * No fixed size.
  * Insertion/removal does not require shifting elements.
* **Disadvantages**:

  * No constant-time random access.
  * Must track length and position manually.
* **Terminology**:

  * **Node**: Individual list element container.
  * **Head**: First node in the list.
  * **Tail**: Last node in the list (null link).
  * **Element**: Stored data in a node.
  * **Link**: Pointer to another node.

---

## 6. **Singly Linked List**

* **Structure**: Each node has one link to the next node.
* **Key Operations**:

  * `addFront()`: Insert at head.
  * `addLast()`: Insert at tail.
  * `removeFront()`: Remove head.
  * `removeLast()`: Remove tail (O(n) without tail pointer).
* **Big Three**: Destructor, Copy Constructor, Assignment Operator (handle dynamic memory).

---

## 7. **Doubly Linked List**

* **Structure**: Nodes have links to both next and previous nodes.
* **Advantage**: Efficient tail removal and bidirectional traversal.
* **Node Structure**: Stores element, `next`, and `prev` pointers.

---

## 8. **Sentinel Nodes**

* **Purpose**: Dummy head and tail nodes to simplify edge cases in insertion/removal.
* **Header/Trailer**: Special sentinels without stored data.

---

## 9. **Circular Linked List**

* **Structure**: Tail links back to head.
* **Cursor**: Pointer to current position in traversal.

---

## 10. **Recursion**

* **Definition**: A function calling itself until a base case is reached.
* **Components**:

  * **Base Case**: Terminates recursion.
  * **Recursive Call**: Processes smaller subproblem.
* **Types**:

  * **Linear Recursion**: One recursive call per activation.
  * **Binary Recursion**: Two recursive calls per activation.
  * **Multiple Recursion**: More than two recursive calls.
  * **Tail Recursion**: Recursive call is the last action; can be optimized into loops.
* **Applications**:

  * Fibonacci sequence.
  * Summation.
  * Linked list algorithms (e.g., recursive delete).

