> 📚 **Prerequisite:** Is se pehle ICT aur programming ke basic concepts (What is computer? Parts of computer, What is hardware?, What is software?, Types of software, What enables us to communicate with hardware?, What enables us to communicate with OS?, What enables OS to communicate with hardware?, Why we create software and what is used to write a software?, What is programming?, What is Progamming language?, Why Programming language?, Types of programming languages, Why high level Programming language?, Variables, Functions, Arrays, conditional statements, Pointers, Structures, etc.) ko samajhna zaroori hai.  
> Ye sab topics yahan cover kiye gaye hain:  
> 👉 [Fundamentals of Programming Repository](https://github.com/Muhammad-Hussain456/Fundamentals_of_Programming-)
> 👉 [Application-of-ICT Repository](https://github.com/Muhammad-Hussain456/Application-of-ICT).


# 🔹 What is OOP?

Object-Oriented Programming (OOP) ek programming paradigm hai jo **objects** par based hai.

Objects contain:
- **Data** (variables / properties)
- **Behavior** (functions / methods)

OOP real-world entities ko program mein represent karne ka tareeqa deta hai.
## 🔹 OOP kyun zaroori?

Pehle hum:

* Har cheez ke liye alag **variables**
* Aur alag **functions** banate thay
  chahy boht sari chezn similar functions and variables ko use kr rahy ho.

👉 Is se problem hoti thi:

* Code repeat hota tha
* Time zyada lagta tha
* Code messy ho jata tha

## ✅ OOP madad karta hai:

* Code ko organized aur modular banata hai
* Code ko maintain aur update karna asaan hota hai
* Code reuse karne mein madad deta hai
* Real-world problems ko asaani se model karta hai
* Bade applications mein complexity kam karta hai

---

# 🔹 Class kyun use karte hain?

Ooper mention problems ko solve karne ke liye OOP mein **class** use ki jati hai.

👉 **Class ek naqsha (نقشہ) / blueprint / template / design hoti hai**

Jisme hum:

* Variables (properties)
* Functions (methods)

ek jagah *define/declare* kar dete hain.

👉 Phir hume baar baar same code likhne ki zaroorat nahi hoti ✅

---

# 🔹 Object kyun use karte hain?

👉 **Object class ka instance (real/physical form) hota hai**

* Class sirf design hai
* Object real cheez hoti hai jo hum use karte hain
* Object mein hum class ke variables aur functions ko initialize karte hain

---

# 🔹 Analogy (Best samajh)

Socho ek **car factory** 🚗

* Class = car ka blueprint/design
* Object = actual car

👉 Tum blueprint ek dafa banate ho
👉 Phir us se bohat sari cars (objects) bana lete ho

Har car:

* Structure same (engine, wheels)
* Lekin color, number different ho sakta hai

---

# 🔹 C++ Example (Bad code - repetition & lengthy)

```cpp id="bad001"
#include <iostream>
using namespace std;

string s1name;
int s1age;
string s2name;
int s2age;
string s3name;
int s3age;
string s4name;
int s4age;

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
    s1age = 20;

    s2name = "Sara";
    s2age = 22;

    s3name = "Hasan";
    s3age = 25;

    s4name = "Hussain";
    s4age = 23;

    s1study();
    s2study();
    s3study();
    s4study();

    return 0;
}
```

---

# 🔹 C++ Example (Good code using Class)

```cpp id="good001"
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int age;

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
    s1.age = 20;

    s2.name = "Sara";
    s2.age = 22;

    s3.name = "Hasan";
    s3.age = 25;

    s4.name = "Hussain";
    s4.age = 23;

    s1.study();
    s2.study();
    s3.study();
    s4.study();

    return 0;
}
```

---

# 🔹 Explanation

👉 Class blueprint hai aur object us blueprint se bani hui real cheez hai

👉 Pehle example mein code repeat hua, lengthy aur difficult tha

👉 Dusre example mein:

* Code clean hai
* Code short hai
* Code reusable hai

👉 `Student` ek class hai

👉 `s1`, `s2`, `s3`, `s4` objects hain

👉 In sab ke paas:

* same properties (name, age)
* same function (study)

---

# 🔹 Benefits of Class & Object

* Code reuse hota hai
* Code repeat nahi hota
* Time bach jata hai
* Code short hota hai
* Code clean aur easy hota hai

---

# 🔹 Repeat vs Reuse

## ❌ Repeat

Same code dobara likhna

## ✅ Reuse

Ek dafa likhna, baar baar use karna

---

# 🔹 Syntax & Semantics

## 🔸 Class Syntax

```cpp id="syn001"
class ClassName {
    // data members
    // member functions
};
```

## 🔸 Class Semantics

* Class ek blueprint hoti hai
* Data aur functions ko group karti hai
* Khud memory allocate nahi karti

---

## 🔸 Object Syntax

```cpp id="syn002"
ClassName objectName;
```

## 🔸 Object Semantics

* Object class ka instance hota hai
* Memory allocate hoti hai
* Har object ki apni values hoti hain

---

# 🔹 OOP ke 4 Pillars

## 1️⃣ Encapsulation

Data ko bundle karna aur protect karna

👉 Example: Bank account (balance private hota hai)

---

## 2️⃣ Abstraction

Sirf zaroori cheez dikhana, baqi hide karna

👉 Example: ATM use karte ho, internal system nahi pata

---

## 3️⃣ Inheritance

Ek class ke features dusri class use kare

👉 Example: BankAccount → SavingsAccount

---

## 4️⃣ Polymorphism

Same function, different behavior

👉 Example: calculateInterest()

---
