# Inheritance in C++

Inheritance is a fundamental concept of **Object-Oriented Programming (OOP)** in C++. It allows a class (derived class) to acquire properties and behaviors (data members and member functions) of another class (base class). This promotes **code reusability**, **extensibility**, and models **real-world hierarchical relationships**.

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

Reuse                                                                                                                                    

Less redundancy                                                                                                                          

Increased maintainability                                                                                                                 
  

---
## Reuse with Inheritance                                                                                                                 
Main purpose of inheritance is reuse                                                                                                      
We can easily add new classes by inheriting from existing classes                                                                        
Select an existing class closer to the desired functionality                                                                              
Create a new class and inherit it from the selected class                                                                                 
Add to and/or modify the inherited functionality                                                                                         

## Inheritance as a Kind of Relationship 

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
