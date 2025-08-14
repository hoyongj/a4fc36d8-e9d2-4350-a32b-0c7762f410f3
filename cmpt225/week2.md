
# 📚 CMPT 225 – Week 2 Key Definitions

## 1. **Control Flow**

* **If Statement**: Executes code based on a condition.
* **Switch Statement**: Selects execution path based on variable value.
* **While Loop**: Repeats while condition is true.
* **Do-While Loop**: Executes at least once, then repeats while condition is true.
* **For Loop**: Loops with initialization, condition, and iteration steps.
* **Break**: Exits loop/switch early.
* **Continue**: Skips to next loop iteration.

---

## 2. **Functions**

* **Function**: A block of code that performs a specific task.
* **Declaration**: Specifies name, return type, and parameters.
* **Definition**: Provides the implementation.
* **Pass by Reference**: Function receives the variable’s reference (`&`), allowing direct modification.
* **Function Overloading**: Multiple functions with same name but different parameter lists.

---

## 3. **C-Style Structures**

* **Struct**: Groups related variables into one type.
* Members accessed using `.` (dot) for objects, `->` for pointers.

---

## 4. **Classes**

* **Class**: Blueprint defining data (**member variables**) and behavior (**member functions**).
* **Public**: Accessible outside the class.
* **Private**: Accessible only within the class.

---

## 5. **The Big 3** (for classes managing dynamic memory)

1. **Destructor**: Frees allocated resources.
2. **Copy Constructor**: Creates a deep copy of another object.
3. **Assignment Operator**: Replaces an object’s contents with another’s, handling memory cleanup and copy.

---

## 6. **Object-Oriented Principles**

* **Abstraction**: Focus on essential features; hide implementation details. Leads to **Abstract Data Types (ADT)** — define what operations do, not how they work.
* **Encapsulation**: Keep data and methods together; hide internal details; control access.
* **Modularity**: Components have distinct purposes and can be reused independently.
* **Hierarchical Organization**: “Is-a” relationships; specialized types derive from general ones.

---

## 7. **Inheritance**

* **Inheritance**: A derived class acquires members from a base class, reducing redundancy.
* **Base Class**: General type.
* **Derived Class**: Specialized type extending the base class.

---

## 8. **Polymorphism**

* **Polymorphism**: Ability for different classes to be treated as instances of the same base type.
* **Overriding**: Derived class provides its own implementation of a base class method.
* **Overloading**: Same method name, different parameter list.
* **Virtual Function**: Enables runtime method resolution (dynamic dispatch).

---

## 9. **Design Patterns**

* Reusable solutions to common design problems.
* Examples: Recursion, Divide and Conquer, Adapter, Iterator, Template Method, Decorator.

---

## 10. **Abstract Classes**

* Cannot be instantiated.
* Have at least one **pure virtual function** (`= 0`).
* Define an interface for derived classes to implement.

---

## 11. **Templates**

* Allow classes and functions to operate with generic types, avoiding code duplication.

---

## 12. **Exceptions**

* **Exception**: Runtime error condition that can be handled with `try-catch`.
* **Throw**: Signal an exception (`throw runtime_error("msg")`).
* **Catch**: Handle an exception (`catch (const runtime_error& e)`).
* **Error vs Exception**:

  * *Error*: Crash-causing, not catchable (e.g., segmentation fault).
  * *Exception*: Catchable runtime issue.

---

## 13. **Arrays and Vectors**

* **Built-in Array**: Fixed-size block of memory; no methods, constructors, or encapsulation.
* **`std::array`**: Fixed-size container with methods (C++ standard library).
* **`std::vector`**: Resizable array-like container with dynamic size management.

