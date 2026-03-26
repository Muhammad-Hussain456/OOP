> 📚 **Prerequisite:** Before this, it is necessary to understand the basic concepts of ICT and programming (What is a computer? Parts of a computer, What is hardware?, What is software?, Types of software, What enables us to communicate with hardware?, What enables us to communicate with the OS?, What enables the OS to communicate with hardware?, Why do we create software and what is used to write software?, What is programming?, What is a programming language?, Why programming languages?, Types of programming languages, Why high-level programming languages?, Variables, Functions, Arrays, Conditional statements, Pointers, Structures, etc.).
> All these topics are covered here:
>                                                                                      
> 👉 [Fundamentals of Programming Repository](https://github.com/Muhammad-Hussain456/Fundamentals_of_Programming-)
>              
> 👉 [Application-of-ICT Repository](https://github.com/Muhammad-Hussain456/Application-of-ICT)

# 🔹 What is Object Oriented Programming(OOP)?                                                                                           
## Object Orientation:
Object orientation is a method or technique of system or thing modeling.                                                                 
## Model:                                                                                                                                 
A model is an abstraction of something. 
## Abstraction 
Abstraction means to show only the necessary implementations or things. 

Example: We first create the model to show neccessary and common/similar things that should be in a car and then build cars following that model.

## Object-Oriented Programming(OOP):
Object-Oriented Programming is a programming technique used to create models for things or systems. It is mainly based on classes and objects.                                                                                                                                 

**For example**, we want to create an attendance system for 50 students. Each student has some common or similar properties (variables) and functions (methods, behavior, or working). We could declare these properties and methods every time for each student, which would take more time, repeat the same code, and make the code lengthy. To fix this issue, we can create a model, template, design, or blueprint for all the students and declare the common or similar properties (variables) and functions (methods, behavior, or working) in that blueprint once. Then, following that blueprint, we can add each student's details to the attendance system. The model, blueprint, design, or template we have created here is known as a **class**. To add each student's details, we create **objects** of that class.

OOP provides a way to represent real-world entities in a program.

## 🔹 Why is OOP necessary?

Before OOP, we used to:

* Create separate **variables** for everything.
* And separate **functions** for everything.
  Even if many things were using the same similar functions and variables.

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

👉 **A class is a map (نقشہ) / blueprint / template / design.**

In it, we:

* Define or declare variables (properties)
* And functions (methods)

in one single place.

👉 Then, we don't need to write the same code repeatedly ✅

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

👉 You create the blueprint once.
👉 Then you can create many cars (objects) from it.

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
