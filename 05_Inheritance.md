# Inheritance in C++

Inheritance is a fundamental concept of **Object-Oriented Programming (OOP)** in C++. It allows a class (derived class) to acquire properties and behaviors (data members and member functions) of another class (base class). This promotes **code reusability**, **extensibility**, and models **real-world hierarchical relationships**.

---

## Main Purpose of Inheritance

The main purpose of inheritance in C++ is to **reuse existing code** and **establish relationships between classes**. By inheriting from a base class, a derived class can:

- Reuse **common properties** and **functions** without rewriting them.
- Increased maintainability.
- Represent **real-world hierarchical relationships** naturally.
- Less redundancy 

---

## Types of Inheritance in C++

1. **Single Inheritance**  
   A derived class inherits from a single base class.

2. **Multiple Inheritance**  
   A derived class inherits from more than one base class.

3. **Multilevel Inheritance**  
   A derived class inherits from another derived class, forming a chain.

4. **Hierarchical Inheritance**  
   Multiple derived classes inherit from a single base class.

5. **Hybrid Inheritance**  
   Combination of two or more types of inheritance.

---


## Example: Person Hierarchy

We can model real-world entities using hierarchical inheritance:

* **Person** (base class)
* **Teacher**, **Doctor**, **Student** (derived classes)

---

### UML Diagram: Person Hierarchy

```text
        +----------------+
        |    Person      |
        +----------------+
        | - name         |
        | - age          |
        | +display()     |
        +----------------+
        /        |       \
       /         |        \
+-----------+ +-----------+ +-----------+
|  Teacher  | |  Doctor   | |  Student  |
+-----------+ +-----------+ +-----------+
| -subject  | | -special. | | -course  |
| +showT()  | | +showD()  | | +showS() |
+-----------+ +-----------+ +-----------+
```

---

## Advantages of Inheritance

1. **Code Reusability** – Write once, use in multiple classes.
2. **Extensibility** – Easily add new classes without modifying existing ones.
3. **Maintainability** – Changes in base class automatically propagate to derived classes.
4. **Polymorphism Support** – Enables dynamic method overriding.
5. **Organized Code** – Helps model real-world relationships in a hierarchical structure.

---
## Reuse with Inheritance                                                                                                                 
Main purpose of inheritance is reuse                                                                                                      
We can easily add new classes by inheriting from existing classes                                                                        
Select an existing class closer to the desired functionality                                                                              
Create a new class and inherit it from the selected class                                                                                 
Add to and/or modify the inherited functionality                                                                                         

## Inheritance as a Kind of Relationship (with UML)

Inheritance represents an **“is-a” relationship** between classes. For example:

* A **Teacher** is a **Person**
* A **Doctor** is a **Person**
* A **Student** is a **Person**

This relationship can be shown using UML:

```text
        +----------------+
        |    Person      |
        +----------------+
        | +display()     |
        +----------------+
        /       |        \
       /        |         \
+-----------+ +-----------+ +-----------+
|  Teacher  | |  Doctor   | |  Student  |
+-----------+ +-----------+ +-----------+
| +showT()  | | +showD()  | | +showS() |
+-----------+ +-----------+ +-----------+
```

**Explanation:**

* The arrow (^) from derived classes points to the base class.
* This “is-a” relationship indicates that derived classes **inherit properties and behavior** of the base class.

---
