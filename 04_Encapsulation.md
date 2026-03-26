# 🔹 Encapsulation

## What is Encapsulation?

**Encapsulation** is a fundamental concept of Object-Oriented Programming (OOP) that bundles data (variables) and methods (functions) together into a single unit and controls access to them.

👉 **Encapsulation = Bundling + Data Hiding + Controlled Access**

---

## 🔹 Two Levels of Encapsulation

Encapsulation exists at two levels in OOP:

| Level | What It Provides | Programming Constructs Used |
|-------|-----------------|---------------------------|
| **Basic Encapsulation** | Bundling data + methods together | Class, Object |
| **True Encapsulation** | Bundling + Data Hiding + Controlled Access | Access Modifiers, Getters, Setters, Validation |

---

# 🔹 Part 1: Basic Encapsulation

## How Class Provides Basic Encapsulation

A **class** itself provides basic encapsulation by:

- **Bundling** properties and functions together
- **Grouping** related properties and behaviors in one place

```cpp
class Student {
    // Data members
    string name;
    int rollNo;
    
    // Member functions
    void study() {
        cout << name << " is studying" << endl;
    }
};
```

👉 Even without access modifiers, the class **bundles** data and methods together.

---

## How Object Provides Basic Encapsulation

An **object** is the physical instance that:

- **Contains** both data and behavior in one unit
- **Represents** a complete entity with its properties and actions

```cpp
int main() {
    Student s1;    // Object encapsulates data + behavior
    
    s1.name = "Ali";
    s1.study();    // Behavior
    
    return 0;
}
```

👉 The object `s1` is a single unit containing both data (`name`) and behavior (`study()`).

---

## 🔹 Basic Encapsulation Example

```cpp
#include <iostream>
using namespace std;

class Student {                    // Class provides bundling
public:
    string name;                   // Data
    int rollNo;                    // Data
    
    void study() {                 // Behavior
        cout << name << " is studying" << endl;
    }
};

int main() {
    Student s1;                    // Object encapsulates everything
    
    s1.name = "Ali";               // Direct access allowed
    s1.rollNo = -5;                // ❌ No validation (problem!)
    s1.study();
    
    return 0;
}
```

### ❌ Problem with Basic Encapsulation:
- Data is exposed directly
- No validation or control
- Invalid data can be assigned
- No security

---

# 🔹 Part 2: True Encapsulation

## What is True Encapsulation?

**True Encapsulation** means:
1. **Bundling** data and methods together (provided by class)
2. **Hiding** data from outside access
3. **Controlling** how data is accessed and modified

---

## Programming Constructs for True Encapsulation

| Construct | Purpose |
|-----------|---------|
| **Access Modifiers** | Hide data from outside |
| **Getter Methods** | Provide controlled read access |
| **Setter Methods** | Provide controlled write access with validation |
| **Validation Logic** | Ensure data integrity |

---

## 1️⃣ Access Modifiers

| Modifier | Access Level | Role in Encapsulation |
|----------|--------------|----------------------|
| **private** | Accessible only within the class | Hides data completely |
| **public** | Accessible from anywhere | Exposes the interface |
| **protected** | Accessible within class and derived classes | Used in inheritance |

---

## 2️⃣ Getter and Setter Methods

| Method Type | Purpose |
|-------------|---------|
| **Getter (Accessor)** | Provides controlled access to read private data |
| **Setter (Mutator)** | Provides controlled access to modify private data |

---

## 3️⃣ Validation Logic

Validation ensures that only **valid data** is stored in the object.

---

## 🔹 True Encapsulation Example

```cpp
#include <iostream>
using namespace std;

class Student {
private:                    // ✅ Data Hiding
    string name;
    int rollNo;
    
public:
    // ✅ Setter with Validation
    void setName(string n) {
        if (!n.empty()) {
            name = n;
        } else {
            cout << "Error: Name cannot be empty!" << endl;
        }
    }
    
    // ✅ Setter with Validation
    void setRollNo(int r) {
        if (r > 0) {
            rollNo = r;
        } else {
            cout << "Error: Roll number must be positive!" << endl;
        }
    }
    
    // ✅ Getter (Controlled Read Access)
    string getName() {
        return name;
    }
    
    // ✅ Getter (Controlled Read Access)
    int getRollNo() {
        return rollNo;
    }
    
    // ✅ Behavior method using private data
    void study() {
        cout << name << " is studying" << endl;
    }
};

int main() {
    Student s1;                    // Object encapsulates data + behavior
    
    // ✅ Controlled access through setters
    s1.setName("Ali");
    s1.setRollNo(101);
    
    // ✅ Controlled read through getters
    cout << "Name: " << s1.getName() << endl;
    cout << "Roll No: " << s1.getRollNo() << endl;
    
    s1.study();
    
    // ❌ Cannot access directly (compilation error)
    // s1.name = "Ahmed";      // Error: private
    // s1.rollNo = 50;         // Error: private
    
    // ✅ Validation prevents invalid data
    s1.setRollNo(-5);           // Error message shown
    
    return 0;
}
```

**Output:**
```
Name: Ali
Roll No: 101
Ali is studying
Error: Roll number must be positive!
```

---

# 🔹 Comparison: Basic vs True Encapsulation

| Feature | Basic Encapsulation | True Encapsulation |
|---------|--------------------|--------------------|
| **Bundling data + methods** | ✅ Yes (via class) | ✅ Yes (via class) |
| **Data Hiding** | ❌ No (data is public) | ✅ Yes (data is private) |
| **Controlled Access** | ❌ No (direct access) | ✅ Yes (via getters/setters) |
| **Validation** | ❌ No | ✅ Yes |
| **Security** | ❌ Low | ✅ High |
| **Data Integrity** | ❌ Not guaranteed | ✅ Guaranteed |
| **Maintainability** | ❌ Difficult | ✅ Easy |

---

# 🔹 Visual Representation

## Basic Encapsulation
```
┌─────────────────────────┐
│         CLASS           │
│  ┌───────────────────┐  │
│  │    Data (public)  │◄─┼── Direct access allowed
│  │    Methods        │  │  (No control)
│  └───────────────────┘  │
└─────────────────────────┘
```

## True Encapsulation
```
┌─────────────────────────────────┐
│             CLASS                │
│  ┌───────────────────────────┐  │
│  │       INTERFACE           │  │
│  │  (Public Methods)         │  │
│  │  ┌─────────────────────┐  │  │
│  │  │ setName()           │  │  │
│  │  │ setRollNo()         │◄─┼── Controlled access
│  │  │ getName()           │  │  │  + Validation
│  │  │ getRollNo()         │  │  │
│  │  └─────────────────────┘  │  │
│  │                           │  │
│  │  ┌─────────────────────┐  │  │
│  │  │   HIDDEN DATA       │  │  │
│  │  │   (private)         │  │  │
│  │  │   - name            │  │  │
│  │  │   - rollNo          │  │  │
│  │  └─────────────────────┘  │  │
│  └───────────────────────────┘  │
└─────────────────────────────────┘
```

---

# 🔹 Rules for True Encapsulation

1. **Declare data members as `private`**
2. **Provide `public` getter methods** for read access
3. **Provide `public` setter methods** for write access
4. **Add validation logic** in setters
5. **Keep internal implementation hidden**
6. **Objects interact only through public methods**

---

# 🔹 Standard Format for True Encapsulation

```cpp
class ClassName {
private:
    // Hidden data members
    dataType variable1;
    dataType variable2;
    
public:
    // Constructor
    ClassName(parameters) {
        // Initialization with validation
    }
    
    // Setter (Mutator) with validation
    void setVariable1(dataType value) {
        if (condition) {
            variable1 = value;
        }
    }
    
    // Getter (Accessor)
    dataType getVariable1() {
        return variable1;
    }
    
    // Behavior methods
    void performAction() {
        // Uses private data
    }
};
```

---

# 🔹 Real-World Analogy

| Real-World | Basic Encapsulation | True Encapsulation |
|------------|--------------------|--------------------|
| **House** | Open house with no doors | House with locked doors and keys |
| **Bank** | Open vault with no security | Vault with PIN, guards, CCTV |
| **Mobile Phone** | No password | Password, fingerprint, face ID |

---

# 🔹 Key Points to Remember

✅ **Basic Encapsulation** comes automatically with class and object (bundling)

✅ **True Encapsulation** requires additional constructs:
   - `private` access modifier (data hiding)
   - Getter methods (controlled read)
   - Setter methods (controlled write)
   - Validation logic (data integrity)

✅ **Class** provides the structure for encapsulation

✅ **Object** is the actual encapsulated unit

✅ **True encapsulation = Security + Control + Data Integrity**

---

# 🔹 Summary

```
ENCAPSULATION
     │
     ├── Basic Encapsulation
     │    ├── Provided by: Class + Object
     │    └── Provides: Bundling of data + methods
     │
     └── True Encapsulation
          ├── Requires: Access Modifiers (private)
          ├── Requires: Getter Methods
          ├── Requires: Setter Methods with Validation
          └── Provides: Bundling + Data Hiding + Controlled Access
```
