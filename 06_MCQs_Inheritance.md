# Inheritance in C++ - Quiz

## Instructions
- Read each question carefully.
- Choose the correct answer from the options provided.
- Click **Check Answer** to reveal the correct response.

---

### Question 1
What is the primary purpose of inheritance in C++ as described in the text?

**A)** To hide data from other classes  
**B)** To reuse existing code and model hierarchical relationships  
**C)** To create multiple instances of a class  
**D)** To overload operators for a class  

<details>
<summary><strong>Check Answer</strong></summary>

**Correct Answer: B**

The text states that inheritance "promotes **code reusability**, **extensibility**, and models **real-world hierarchical relationships**."
</details>

---

### Question 2
Based on the provided example, which of the following best describes the relationship between a `Teacher` and a `Person`?

**A)** A `Person` is a `Teacher`  
**B)** A `Teacher` has a `Person`  
**C)** A `Teacher` is a `Person`  
**D)** A `Teacher` uses a `Person`  

<details>
<summary><strong>Check Answer</strong></summary>

**Correct Answer: C**

The text explicitly states that inheritance represents an "is-a relationship" and gives the example: "A **Teacher** is a **Person**."
</details>

---

### Question 3
In the UML diagram provided for the Person hierarchy, what does the arrow (pointing from `Teacher` to `Person`) signify?

**A)** That `Teacher` contains a `Person` object  
**B)** That `Teacher` inherits from `Person`  
**C)** That `Person` inherits from `Teacher`  
**D)** That the two classes are unrelated  

<details>
<summary><strong>Check Answer</strong></summary>

**Correct Answer: B**

The text explains: "The arrow (^) from derived classes points to the base class." This indicates that the derived class (`Teacher`) inherits from the base class (`Person`).
</details>

---

### Question 4
Which of the following is NOT listed as an advantage of inheritance in the text?

**A)** Reuse  
**B)** Less redundancy  
**C)** Increased maintainability  
**D)** Faster runtime execution  

<details>
<summary><strong>Check Answer</strong></summary>

**Correct Answer: D**

The text lists "Reuse," "Less redundancy," and "Increased maintainability" as advantages. It does not mention faster runtime execution as an inherent advantage of inheritance.
</details>

---

### Question 5
In the provided class hierarchy (`Person`, `Teacher`, `Doctor`, `Student`), which member function is most likely inherited from the base class?

**A)** `showT()`  
**B)** `showD()`  
**C)** `display()`  
**D)** `showS()`  

<details>
<summary><strong>Check Answer</strong></summary>

**Correct Answer: C**

In the UML diagram, the `display()` function is listed in the `Person` class, while `showT()`, `showD()`, and `showS()` are listed only in their respective derived classes. Therefore, `display()` is the function inherited by `Teacher`, `Doctor`, and `Student`.
</details>

---

### Question 6
What is a key step in adding a new class using inheritance according to the "Reuse with Inheritance" section?

**A)** Delete all existing classes before adding a new one  
**B)** Select an existing class close to the desired functionality and inherit from it  
**C)** Write the new class from scratch without referencing existing code  
**D)** Copy the code from an existing class and rename it  

<details>
<summary><strong>Check Answer</strong></summary>

**Correct Answer: B**

The text outlines the process: "Select an existing class closer to the desired functionality... Create a new class and inherit it from the selected class."
</details>
