# 🔹 Declaration and Initialization of Object                                                                                                                                                                                                 
## 🔹 Declaration of Object
Creating an object is called declaration of object.                              

When an object is declared, it gets the properties and functions declared in the class.
### Syntax:
```cpp
ClassName objectName;
```

### Example:
```cpp
Student s1;    // s1 is an object of Student class
```

---

## 🔹 Initialization of Object

Initialization means giving values to the object's data members.                                                                                                                                   
After declaring the object, we can assign values to its members.

---

### 1️⃣ **Using Dot Operator (.)**

This is the simplest way. After declaring the object, use dot (.) to assign values.

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int rollNo;
};

int main() {
    Student s1;                    // Declaration
    
    // Initialization using dot operator
    s1.name = "Ali";
    s1.rollNo = 101;
    
    cout << s1.name << endl;       // Output: Ali
    cout << s1.rollNo << endl;     // Output: 101
    
    return 0;
}
```

---

### 2️⃣ **Using Constructor**

A **constructor** is a special function that automatically initializes an object when it is created.

#### a) **Parameterized Constructor** 

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int rollNo;
    
    // Constructor (same name as class)
    Student(string n, int r) {
        name = n;
        rollNo = r;
    }
};

int main() {
    // Declaration + Initialization in one line
    Student s1("Ali", 101);
    Student s2("Sara", 102);
    
    cout << s1.name << " - " << s1.rollNo << endl;  // Output: Ali - 101
    cout << s2.name << " - " << s2.rollNo << endl;  // Output: Sara - 102
    
    return 0;
}
```

#### b) **Default Constructor**

When we want default values if nothing is provided.

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int rollNo;
    
    // Default Constructor
    Student() {
        name = "Unknown";
        rollNo = 0;
    }
};

int main() {
    Student s1;                    // Automatically gets default values
    
    cout << s1.name << endl;       // Output: Unknown
    cout << s1.rollNo << endl;     // Output: 0
    
    return 0;
}
```
---

## 🔹 Most Common Ways 

| # | Method | Code Example |
|---|--------|--------------|
| 1 | **Dot Operator** | `s1.name = "Ali";` |
| 2 | **Constructor** | `Student s1("Ali", 101);` |

---

## 🔹 Key Points to Remember

✅ **Dot Operator** is simplest for beginners  
✅ **Constructor** is the most professional and widely used  
✅ Declaration + Initialization can be done in one line using constructors  

---

## 🔹 Quick Comparison

```cpp
// Way 1: Dot Operator
Student s1;
s1.name = "Ali";
s1.rollNo = 101;

// Way 2: Constructor 
Student s1("Ali", 101);

```

---
