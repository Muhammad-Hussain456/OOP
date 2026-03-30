# 🔹 Encapsulation

## What is Encapsulation?

**Encapsulation** is a fundamental concept of Object-Oriented Programming (OOP) that bundles/groups data (variables) and methods (functions) together into a single unit and controls access to them.

👉 **Encapsulation = Bundling/Grouping + Data Hiding + Controlled Access**

---

## 🔹 Two Levels of Encapsulation

Encapsulation exists at two levels in OOP:

| Level | What It Provides | Programming Constructs Used |
|-------|-----------------|---------------------------|
| **Basic Encapsulation** | Bundling/Grouping data and methods together | Class, Object |
| **True Encapsulation** | Bundling/Grouping , Data Hiding and Controlled Access | Access Modifiers, Getters, Setters, Validation |

---

# 🔹 Part 1: Basic Encapsulation

## How Class Provides Basic Encapsulation

A **class** itself provides basic encapsulation by:

- **Bundling/Grouping** related properties and behaviors/functions/methods in one place

```cpp
class Student {
    // Data members / properties
    string name;
    int rollNo;
    
    // Member functions / methods 
    void study() {
        cout << name << " is studying" << endl;
    }
};
```

👉 Even without access modifiers, the class **bundles** data and methods together.

---

## How Object Provides Basic Encapsulation

An **object** is the physical instance that:

- **Contains** both data/properties and behavior/function in one unit
- **Represents** a complete entity with its properties and actions

```cpp
int main() {
    Student s1;    // object
    
    s1.name = "Ali";
    s1.study();    // method
    
    return 0;
}
```

👉 The object `s1` is a single unit containing both data/properties (`name`) and behavior/method/function (`study()`).

---

## 🔹 Basic Encapsulation Example

```cpp
#include <iostream>
using namespace std;

class Student {                    // Class provides bundling/grouping
public:
    string name;                   // Data/property/attribute/member
    int rollNo;                    // Data/property/attribute/member
    
    void study() {                 // method
        cout << name << " is studying" << endl;
    }
};

int main() {
    Student s1;                              
    
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



### 🔹 private
Accessible only within the same class.

```cpp
class Person {
private:
    int age = 25;
};
````

---

### 🔹 public

Accessible from anywhere.

```cpp
#include <iostream>
using namespace std;

class Person {
public:
    string name = "Ali";
};
```

---

### 🔹 protected

Accessible within the class and derived classes.

```cpp
#include <iostream>
using namespace std;

class Parent {
protected:
    int value = 10;
};
```

---

## 2️⃣ Getter and Setter Methods

| Method Type | Purpose |
|-------------|---------|
| **Getter (Accessor)** | Provides controlled access to read private data |
| **Setter (Mutator)** | Provides controlled access to modify private data |

### 🔹 Getter (Accessor)

Used to read private data.

```cpp
class Person {
private:
    string name;

public:
    string getName() {
        return name;
    }
};
```

---

### 🔹 Setter (Mutator)

Used to modify private data.

```cpp
class Person {
private:
    string name;

public:
    void setName(string n) {
        name = n;
    }
};
```
---

## 3️⃣ Validation Logic

Validation ensures that only **valid data** is stored in the object.                                                                      
Use if/else conditions inside setters                                                                                                     
Prevent invalid data assignment                                                                                                           
Improves data safety and encapsulation

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
│  │                           │  │
│  │        (Public)           │  │
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

# 🔹 Real-World Analogy

| Real-World | Basic Encapsulation | True Encapsulation |
|------------|--------------------|--------------------|
| **House** | Open house with no doors | House with locked doors and keys |
| **Bank** | Open vault with no security | Vault with PIN, guards, CCTV |
| **Mobile Phone** | No password | Password, fingerprint, face ID |

---

# 🔹 Key Points to Remember

✅ **Basic Encapsulation** comes automatically with class and object (bundling/grouping)

✅ **True Encapsulation** requires additional constructs:
   - `private` access modifier (data hiding)
   - Getter methods (controlled read)
   - Setter methods (controlled write)
   - Validation logic (data integrity)


---


## 📋 Example Problem: Student Grade Management System

### Problem Statement
Write a program to build a Student Grade Management System.

## Solution

### Define the problem
A school needs a system to manage student grades. The system must ensure that:
- Student marks are always between 0 and 100
- A student cannot have a negative roll number
- The student's name cannot be empty
- The grade is automatically calculated based on marks
- Once a student is created, their details should be protected from invalid modifications

---

## 🔍 Analysis

### Requirements Identification

| Requirement Type | Details |
|-----------------|---------|
| **Data to Store** | Student name, roll number, marks, grade |
| **Operations** | Create student, update marks, view details |
| **Constraints/Limits** | Name: non-empty, Roll No: positive, Marks: 0-100 |
| **Business Logic** | Grade calculation based on marks |

### Grade Calculation Rule
```
Marks >= 90  → Grade: A+
Marks >= 80  → Grade: A
Marks >= 70  → Grade: B
Marks >= 60  → Grade: C
Marks >= 50  → Grade: D
Marks < 50   → Grade: F
```

### Encapsulation Requirements
1. **Data/Property Hiding**: All data members(properties) must be private
2. **Controlled Access**: Getters and setters with validation
3. **Automatic Updates**: Grade updates automatically when marks change
4. **Data Integrity**: No invalid data can be stored

---

## 🧮 Algorithm

### 📋 Step 1: Create the Student Blueprint/Class

First, we create a **Student blueprint** (called a class) that will store:
- **Name** - what the student is called
- **Roll Number** - the student's ID number
- **Marks** - the student's score
- **Grade** - the letter grade (A+, A, B, etc.)

**Important:** We hide these details so nobody can change them directly.

---

### 📋 Step 2: Create Methods (Setters) to Set properties/data 

We need **special doors** (called setters) to put information/value into properties/data/attributes of objects(students).
We use this method as we want to have control over the changes.

#### Setting the Name:
```
When we want to set the name:
    → First check: Is the name empty?
    → If NOT empty: Save the name
    → If empty: Show error message "Name cannot be empty"
```

#### Setting the Roll Number:
```
When we want to set the roll number:
    → First check: Is the number greater than 0?
    → If YES: Save the roll number
    → If NO: Show error message "Roll number must be positive"
```

#### Setting the Marks:
```
When we want to set the marks:
    → First check: Are marks between 0 and 100?
    → If YES: 
        - Save the marks
        - Automatically calculate the grade
    → If NO: Show error message "Marks must be between 0 and 100"
```

---

### 📋 Step 3: Create Methods to Get Information (Getters)

We create **special windows** (called getters) to look at the information/values:
We use this method as we want to control read access.
```
getName()    → Just give me the name
getRollNo()  → Just give me the roll number  
getMarks()   → Just give me the marks
getGrade()   → Just give me the grade
```

These are like **read-only** - you can see but cannot change!

---

### 📋 Step 4: Create Grade Calculation Logic

```
This is our rule book for grades:

If marks are 90 or above    → Grade is "A+"
If marks are 80 to 89       → Grade is "A"
If marks are 70 to 79       → Grade is "B"
If marks are 60 to 69       → Grade is "C"
If marks are 50 to 59       → Grade is "D"
If marks are below 50       → Grade is "F"
```

**Important:** This happens automatically whenever marks change!

---

### 📋 Step 5: Create Display/Output Method

```
When we want to see all student information:
    → Show the name
    → Show the roll number
    → Show the marks
    → Show the grade
    → Print a nice line to separate
```

---

### 📋 Step 6: Test Everything (Main Program)

Now we test our student system:

#### Test 1: Create a student object with Good Information/values
```
Make a new student called "Ali Raza" with roll number 101 and 85.5 marks
Show the student's information
Expected: Everything looks correct with grade "A"
```

#### Test 2: Try to Put Wrong Information/values
```
Try to give the student 150 marks
    → The system should say "Error: Marks must be between 0 and 100"
    → The old marks should stay (85.5)
    → Grade should not change
```

#### Test 3: Put Good Information and Watch Grade Update/Change
```
Give the student 92.5 marks
    → System accepts because it's between 0-100
    → Grade automatically changes to "A+"
    → Show the updated information
```

#### Test 4: Try to Create student object with Bad Information/Values
```
Try to make a student with:
    - Empty name
    - Negative roll number (-5)
    - 75 marks
    
The system should:
    → Show error about empty name, use "Unknown" instead
    → Show error about negative roll number, use 0 instead
    → Accept the marks (75 is valid)
    → Calculate grade "B" for 75 marks
```
---

## 💻 Program Implementation

### C++ Program with True Encapsulation

```cpp
#include <iostream>
#include <string>
using namespace std;

class Student {
private:
    // Hidden data members
    string name;
    int rollNo;
    float marks;
    string grade;
    
    // Private helper method for grade calculation
    void calculateGrade() {
        if (marks >= 90) {
            grade = "A+";
        } else if (marks >= 80) {
            grade = "A";
        } else if (marks >= 70) {
            grade = "B";
        } else if (marks >= 60) {
            grade = "C";
        } else if (marks >= 50) {
            grade = "D";
        } else {
            grade = "F";
        }
    }
    
public:
    // Constructor with validation
    Student(string n, int r, float m) {
        setName(n);
        setRollNo(r);
        setMarks(m);  // This will also calculate grade
    }
    
    // Setter for name with validation
    void setName(string n) {
        if (!n.empty()) {
            name = n;
        } else {
            cout << "Error: Name cannot be empty!" << endl;
            name = "Unknown";
        }
    }
    
    // Setter for roll number with validation
    void setRollNo(int r) {
        if (r > 0) {
            rollNo = r;
        } else {
            cout << "Error: Roll number must be positive!" << endl;
            rollNo = 0;
        }
    }
    
    // Setter for marks with validation and auto grade update
    void setMarks(float m) {
        if (m >= 0 && m <= 100) {
            marks = m;
            calculateGrade();  // Grade automatically updates
        } else {
            cout << "Error: Marks must be between 0 and 100!" << endl;
            marks = 0;
            calculateGrade();
        }
    }
    
    // Getters for controlled read access
    string getName() {
        return name;
    }
    
    int getRollNo() {
        return rollNo;
    }
    
    float getMarks() {
        return marks;
    }
    
    string getGrade() {
        return grade;
    }
    
    // Method to display student information
    void displayInfo() {
        cout << "\n--- Student Information ---" << endl;
        cout << "Name    : " << name << endl;
        cout << "Roll No : " << rollNo << endl;
        cout << "Marks   : " << marks << endl;
        cout << "Grade   : " << grade << endl;
        cout << "---------------------------" << endl;
    }
};

int main() {
    cout << "===== Student Grade Management System =====" << endl;
    cout << "Demonstrating True Encapsulation\n" << endl;
    
    // Creating student with valid data
    cout << "1. Creating student with valid data:" << endl;
    Student s1("Ali Raza", 101, 85.5);
    s1.displayInfo();
    
    // Demonstrating validation
    cout << "\n2. Trying to set invalid marks:" << endl;
    s1.setMarks(150);  // Invalid - will show error
    s1.displayInfo();   // Shows marks unchanged
    
    cout << "\n3. Setting valid marks:" << endl;
    s1.setMarks(92.5);  // Valid - grade auto updates
    s1.displayInfo();   // Shows updated marks and grade
    
    // Creating student with invalid data
    cout << "\n4. Creating student with invalid data:" << endl;
    Student s2("", -5, 75);  // Invalid name and roll number
    s2.displayInfo();   // Shows default values with errors
    
    // Demonstrating controlled access
    cout << "\n5. Controlled access demonstration:" << endl;
    cout << "Student name: " << s1.getName() << endl;
    cout << "Student grade: " << s1.getGrade() << endl;
    
    // This would cause error if uncommented (data hiding)
    // s1.marks = 95;  // Error: marks is private
    
    // Testing grade boundaries
    cout << "\n6. Testing grade boundaries:" << endl;
    Student s3("Test Student", 103, 89);
    s3.displayInfo();
    
    s3.setMarks(90);
    cout << "\nAfter updating marks to 90:" << endl;
    s3.displayInfo();
    
    return 0;
}
```

---

## 📊 Program Output

```
===== Student Grade Management System =====
Demonstrating True Encapsulation

1. Creating student with valid data:

--- Student Information ---
Name    : Ali Raza
Roll No : 101
Marks   : 85.5
Grade   : A
---------------------------

2. Trying to set invalid marks:
Error: Marks must be between 0 and 100!

--- Student Information ---
Name    : Ali Raza
Roll No : 101
Marks   : 85.5
Grade   : A
---------------------------

3. Setting valid marks:

--- Student Information ---
Name    : Ali Raza
Roll No : 101
Marks   : 92.5
Grade   : A+
---------------------------

4. Creating student with invalid data:
Error: Name cannot be empty!
Error: Roll number must be positive!

--- Student Information ---
Name    : Unknown
Roll No : 0
Marks   : 75
Grade   : B
---------------------------

5. Controlled access demonstration:
Student name: Ali Raza
Student grade: A+

6. Testing grade boundaries:

--- Student Information ---
Name    : Test Student
Roll No : 103
Marks   : 89
Grade   : A
---------------------------

After updating marks to 90:

--- Student Information ---
Name    : Test Student
Roll No : 103
Marks   : 90
Grade   : A+
---------------------------
```

---


## 🔍 Explanation (How Encapsulation is Applied)

### 1. **Bundling** (Basic Encapsulation)
```cpp
class Student {
    // Data and methods bundled together
private:
    string name;      // data
    int rollNo;       // data
    float marks;      // data
    string grade;     // data
    
    void calculateGrade() { }  // method
public:
    void setName() { }          // method
    void setMarks() { }         // method
    // ...
};
```

### 2. **Data Hiding** (Access Modifiers)
```cpp
private:
    string name;      // Hidden from outside
    int rollNo;       // Hidden from outside
    float marks;      // Hidden from outside
```

### 3. **Controlled Access** (Getters & Setters)
```cpp
public:
    void setMarks(float m) {    // Controlled write access
        if (m >= 0 && m <= 100) {
            marks = m;
            calculateGrade();
        }
    }
    
    float getMarks() {          // Controlled read access
        return marks;
    }
```

### 4. **Validation Logic**
```cpp
if (m >= 0 && m <= 100) {
    // Valid - update
} else {
    // Invalid - show error
}
```

---

## 📈 Benefits Achieved

| Benefit | How It's Achieved |
|---------|------------------|
| **Data Security** | Private data members/properties prevent direct access |
| **Data Integrity** | Validation ensures only valid data/property is stored |
| **Automatic Updates** | Grade auto-calculates when marks change |
| **Maintainability** | Changes to validation logic only affect setters |
| **Controlled Interface** | Clear public methods define how to interact |
| **Error Prevention** | Invalid inputs are caught and handled |

---



# 🔹 Summary

1. **Basic encapsulation** comes automatically with class bundling
2. **True encapsulation** requires private members + getters/setters
3. **Validation** is essential for data integrity
4. **Business logic** (like grade calculation) stays inside the class
5. **Objects** become self-contained, reliable units
