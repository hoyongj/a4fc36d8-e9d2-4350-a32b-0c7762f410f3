Here’s a **definition summary** of the two uploaded week 4 files, keeping only the concepts introduced in them and avoiding any previous week content:

---

## **Algorithm Analysis & Big-O**

* **Algorithm Analysis** – Study of algorithm efficiency in terms of time and/or space.
* **Experimental Approach** – Measuring runtime by running the algorithm with various inputs; limited by hardware, sample size, and implementation details.
* **Theoretical Analysis** – Predicting runtime from pseudocode by counting primitive operations, independent of hardware.
* **Primitive Operations** – Basic actions like assignments, arithmetic operations, comparisons, indexing, method calls, returning values.
* **Seven Common Growth Rates** –

  1. **Constant**: $O(1)$ – Time does not change with input size.
  2. **Logarithmic**: $O(\log n)$ – Time grows slowly, e.g., binary search.
  3. **Linear**: $O(n)$ – Time proportional to input size.
  4. **N-Log-N**: $O(n\log n)$ – Often from efficient sorting.
  5. **Quadratic**: $O(n^2)$ – Nested loops over data.
  6. **Cubic/Polynomial**: $O(n^k)$ – Higher-degree nested processing.
  7. **Exponential**: $O(b^n)$ – Grows too fast for large inputs.
* **Worst-Case Scenario** – Upper bound of runtime for the hardest inputs.
* **Asymptotic Analysis** – Focuses on fastest-growing term of runtime for large $n$.
* **Big-O Notation (O)** – Upper bound on growth rate.
* **Big-Omega (Ω)** – Lower bound on growth rate.
* **Big-Theta (Θ)** – Tight bound; both upper and lower bounds match.
* **Big-O Rules** – Use smallest class, drop lower-order terms, drop constant factors.
* **Tips for Analysis** – Identify $n$, work from innermost loops outward, account for function calls and worst-case branches.

---

## **Stacks**

* **Stack (ADT)** – A collection of elements with **First-In, Last-Out (FILO)** order.
* **Core Operations**:

  * **push(x)** – Add to top.
  * **pop()** – Remove from top.
  * **top()** – Return top without removing.
  * **size()** – Number of elements.
  * **isEmpty()** – Check if stack is empty.
* **Implementations**:

  * **Array-Based Stack** – Fixed-size storage; push/pop at end.
  * **Linked List Stack** – Dynamic size; push/pop at head.
* **C++ Standard Library** – Provides `std::stack` (based on `deque` by default).
* **Performance (Typical Big-O)** – All operations $O(1)$ on both array and linked list implementations.
* **Common Uses**:

  * Undo functionality.
  * Browser back button.
  * Parsing/matching symbols (e.g., parentheses).

---

If you want, I can also make you a **condensed one-page quick reference sheet** from this so it’s faster to study. That would turn this into a very compact exam-ready handout.
