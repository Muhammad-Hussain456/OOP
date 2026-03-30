# Abstraction in C++

Abstraction is one of the **core concepts of Object-Oriented Programming (OOP)** in C++. It allows a programmer to **hide the internal implementation details** of a class or function and show only the essential features to the user. In simpler words, abstraction focuses on **what an object does**, rather than **how it does it**.

---

## Key Points

- **Purpose**: To reduce complexity and isolate the impact of changes.
- **How achieved**: Using **abstract classes** and **interfaces** (pure virtual functions) in C++.
- **Benefits**:
  - Hides unnecessary details from the user.
  - Helps in **maintaining large codebases**.
  - Enhances **security** and **code reusability**.

---

## Abstract Classes

An **abstract class** is a class that **cannot be instantiated** and usually contains **at least one pure virtual function**.
````

* `= 0` indicates a **pure virtual function**.
* Classes inheriting an abstract class **must implement** all pure virtual functions to become concrete.

---
`

**Explanation:**

* `Shape` is an **abstract class** with a pure virtual function `draw()`.
* `Circle` and `Rectangle` **implement the draw() function**.
* The user can **use the abstract interface `Shape`** without knowing the details of `Circle` or `Rectangle`.

---

## When to Use Abstraction

* When you want to **hide internal details** of a class.
* When you want to define a **common interface** for different types of objects.
* To **simplify code maintenance** and improve **modularity**.

---

## Key Differences: Abstraction vs Encapsulation

| Feature        | Abstraction                                            | Encapsulation                                                              |
| -------------- | ------------------------------------------------------ | -------------------------------------------------------------------------- |
| Focus          | Hides **implementation details**                       | Hides **data**                                                             |
| Implementation | Achieved using **abstract classes** and **interfaces** | Achieved using **access specifiers** (private, protected, public)          |
| Example        | Abstract class `Shape` with pure virtual functions     | Class `Car` with private variables like `speed` and public getters/setters |

---

Abstraction in C++ ensures that the **complex implementation details** are hidden, providing a **clean and simple interface** to the user.

```

If you want, I can also **add diagrams in Markdown** to visually show abstraction in C++ classes. It makes the file look more professional. Do you want me to do that?
```
