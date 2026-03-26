📚 **Prerequisite:** Before this, it is necessary to understand the basic concepts of ICT and programming (What is a computer? Parts of a computer, What is hardware?, What is software?, Why do we create software and what is used to write software?, What is programming?, What is a programming language?, Why programming languages?, Types of programming languages, Why high-level programming languages?, Variables, Functions, Arrays, Conditional statements, Pointers, Structures, etc.). All these topics are covered here:

👉 [Fundamentals of Programming Repository](https://github.com/Muhammad-Hussain456/Fundamentals_of_Programming-)

👉 [Application-of-ICT Repository](https://github.com/Muhammad-Hussain456/Application-of-ICT)

# 🔹 What is Object Oriented Programming(OOP)?

## Object Orientation:
Object orientation is a method or technique of system or thing modeling.

## Model:
A model is an abstraction of something.

## Abstraction
Abstraction means to show only the necessary implementations or things.

**Example:** A company first creates the model to show neccessary common/similar properties and workings/functions that should be their cars and then build cars following that model.

## Object-Oriented Programming(OOP):
Object-Oriented Programming is a programming technique used to create models for things or systems. It is mainly based on classes and objects.

**For example**, we want to create an attendance system for 50 students. Each student has some common or similar properties (variables) and functions (methods, behavior, or working). We could declare these properties and methods every time for each student, which would take more time, repeat the same code, and make the code lengthy. To fix this issue, we can create a model, template, design, or blueprint for all the students and declare the common or similar properties (variables) and functions (methods, behavior, or working) in that blueprint once. Then, following that blueprint, we can add each student's details to the attendance system. The model, blueprint, design, or template we have created here is known as a **class**. To add each student's details, we create **objects** of that class.

OOP provides a way to represent real-world entities in a program.

## 🔹 Why is OOP necessary?

Before OOP, we used to:

* Create separate **variables** for everything.
* And separate **functions** for everything. Even if many things were using the same similar functions and variables.

👉 This led to problems:

* Code repetition.
* More time consumption.
* Code became messy.

## ✅ OOP helps by:

* Making the code organized and modular.
* Making code easier to maintain and update.
* Helping with code reuse.
* Making it easier to model real-world problems.
* Reducing complexity in large applications.

---

# 🔹 Why do we use a Class?

To solve the problems mentioned above, we use a **class** in OOP.

👉 **A class is a map (نقشہ) / blueprint / template / design/ model.**

In it, we:

* Define or declare variables (properties) and functions (methods) in one single place. Then, we don't need to write the same code repeatedly.

---

# 🔹 Why do we use an Object?

👉 **An object is an instance (real/physical form) of a class.**

* The class is just a design.
* The object is the real thing that we use.
* In the object, we initialize the variables and functions defined in the class.

---

# 🔹 Analogy (Best way to understand)

Think of a **car factory** 🚗

* Class = The car's blueprint or design.
* Object = The actual car.

👉 You create the blueprint once. 👉 Then you can create many cars (objects) from it.

Each car:

* Has the same structure (engine, wheels).
* But can have different colors, registration numbers, etc.

---

# 🔹 C++ Example (Bad code - repetition & lengthy)

```cpp
#include <iostream>
using namespace std;

string s1name;
int s1RollNo;
string s2name;
int s2RollNo;
string s3name;
int s3RollNo;
string s4name;
int s4RollNo;

void s1study() {
    cout << s1name << " is studying" << endl;
}

void s2study() {
    cout << s2name << " is studying" << endl;
}

void s3study() {
    cout << s3name << " is studying" << endl;
}

void s4study() {
    cout << s4name << " is studying" << endl;
}

int main() {

    s1name = "Ali";
    s1RollNo = 20;

    s2name = "Sara";
    s2RollNo = 22;

    s3name = "Hasan";
    s3RollNo = 25;

    s4name = "Hussain";
    s4RollNo = 23;

    s1study();
    s2study();
    s3study();
    s4study();

    return 0;

}
```

---

# 🔹 C++ Example (Good code using Class)

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int RollNo;

    void study() {
        cout << name << " is studying" << endl;
    }
};

int main() {
    Student s1;
    Student s2;
    Student s3;
    Student s4;

    s1.name = "Ali";
    s1.RollNo = 20;

    s2.name = "Sara";
    s2.RollNo = 22;

    s3.name = "Hasan";
    s3.RollNo = 25;

    s4.name = "Hussain";
    s4.RollNo = 23;

    s1.study();
    s2.study();
    s3.study();
    s4.study();

    return 0;
}
```

---

# 🔹 Explanation

👉 The class is the blueprint, and the object is the real thing created from that blueprint.

👉 In the first example, the code is repeated, lengthy, and difficult.

👉 In the second example:

* The code is clean.
* The code is short.
* The code is reusable.

👉 `Student` is a class.

👉 `s1`, `s2`, `s3`, and `s4` are objects.

👉 All of them have:

* The same properties (`name`, `RollNo`).
* The same function (`study`).

---

# 🔹 Benefits of Class & Object

* Code is reused.
* Code is not repeated.
* Time is saved.
* Code is short.
* Code is clean and easy to manage.

---

# 🔹 Repeat vs Reuse

## ❌ Repeat

Writing the same code again.

## ✅ Reuse

Writing something once and using it multiple times.

---

# 🔹 Syntax & Semantics

## 🔸 Class Syntax

```cpp
class ClassName {
    // variable/members/properties/attributes
    // member functions/methods
};
```

## 🔸 Class Semantics

* A class is a blueprint.
* It groups data and functions together.
* It does not allocate memory by itself.

---

## 🔸 Object Syntax

```cpp
ClassName objectName;
```

## 🔸 Object Semantics

* An object is an instance of a class.
* Memory is allocated for it.
* Each object has its own values for the data members.

---


This is the main syntax, and additional programming constructs such as OOP's 4 pillars are added to it based on the nature of the problem. In most cases, OOP uses the 4 pillars (Encapsulation, Inheritance, Polymorphism, Abstraction) with classes and objects main as needed by the problem. Sometimes only encapsulation is needed, sometimes only polymorphism, sometimes inheritance, and sometimes abstraction. Sometimes two, three, or all four pillars have to be used — this all depends on the nature of the problem.

# 🔹 The 4 Pillars of OOP

## 1️⃣ Encapsulation

 Used for Bundling, Data Hiding and Controlled Access

**Note:** Basic encapsulation (bundling) is automatically used whenever we create a class and object because a class groups data and methods together. 
However, for **true encapsulation** (data hiding + controlled access), we need additional programming constructs.

Without these, the class is just a container, not truly encapsulated.

👉 Example: PINs, passwords, bank account balances, etc., are kept private.

**How to use/implement encapsulation in program**                                                                                         
using access modifiers (private, public, protected), getter and setter methods, and classes

---

## 2️⃣ Abstraction
Used for implementation hiding.                                                                                                           
Abstraction = Hiding complex implementation details                                                                                       
Showing only the necessary things and hiding the rest.

👉 Example: You use an ATM, but you don't know its internal system. Users use app icons, folders, and files, but the internal programming is not shown to them.

**How to use/implement abstraction in program**                                                                                           
using abstract classes, interfaces, pure virtual functions, and abstract methods

---

## 3️⃣ Inheritance
One class uses the features of another class.

it creates parent child relationship between two or more classes.

👉 Example: BankAccount → SavingsAccount

**How to use/implement inheritance in program**                                                                                           
using base class (parent class), derived class (child class), and inheritance syntax (extends in Java, : in C++)

---

## 4️⃣ Polymorphism
Same function name, different behavior/working.

👉 Example: calculateInterest()

**How to use/implement polymorphism in program**                                                                                          
using method overloading, method overriding, virtual functions, operator overloading, function overloading, and interfaces

---
