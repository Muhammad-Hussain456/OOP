# Class Structure: Properties and Methods (C++)

---

## Class Structure Overview

A class in Object-Oriented Programming (OOP) is composed of two main components:

| Component  | Also Known As                    | Purpose                           |
|------------|----------------------------------|-----------------------------------|
| Properties | Attributes, Data Members, Fields | Store the state/data  |
| Methods    | Member Functions, Behaviors      | Define actions  |

### Example

```cpp
class Student {
    // Properties (Data Members)
    string name;
    int rollNo;
    float GPA;

    // Methods (Member Functions)
};
```

---

## Member Functions (Methods)

Member functions are functions declared or defined inside a class that operate on data members of the class.

### Key Points

- Define behavior of objects  
- Have access to all class members  
- Public methods act as the interface of the class  

---

## Defining Member Functions

Member functions can be defined in two ways:

---

### 1. Inside Class Definition

Functions defined inside the class are **implicitly inline**.

```cpp
class ClassName {
public:
    ReturnType functionName() {
        // code
    }
};
```

#### Example

```cpp
class Student {
    int rollNo;
public:
    void setRollNo(int aRollNo) {
        rollNo = aRollNo;
    }
};
```

---

### 2. Outside Class Definition

Declared inside class and defined outside using the scope resolution operator `::`.

#### Syntax

```cpp
class ClassName {
public:
    ReturnType functionName();  // Declaration
};

ReturnType ClassName::functionName() {
    // definition
}
```

#### Example

```cpp
class Student {
    int rollNo;
public:
    void setRollNo(int aRollNo);
};

void Student::setRollNo(int aRollNo) {
    rollNo = aRollNo;
}
```

---

## 🔹 Inline Functions 

An inline function is a function whose code is inserted at the point of call instead of a normal function to reduce function call overhead.                                                                                                  
overhead = extra work/time.                                                                                              
If we define the function inside the class body then the function is by default an inline function.                      
If function is defined outside the class body then we must use the keyword ‘inline’ to make a function inline.


---

### 🔹 Example 1: Function Defined Inside Class (Default Inline)

```cpp
class Student {
    int rollNo;

public:
    void setRollNo(int aRollNo) {   // implicitly inline
        rollNo = aRollNo;
    }
};
```

---

### 🔹 Example 2: Function Defined Outside Class (Explicit Inline)

```cpp
class Student {
    int rollNo;

public:
    void setRollNo(int aRollNo);
};

inline void Student::setRollNo(int aRollNo) {
    rollNo = aRollNo;
}
```

---

### ⚠️ Important Note

- `inline` is a **request**, not a command  
- The compiler may **ignore it**
  


---

## Constructors

Constructors are special member functions used to initialize objects automatically at creation.

### Characteristics

| Feature      | Description                  |
|--------------|---------------------------|
| Name         | Same as class name           |
| Return Type  | None (not even void)         |
| Calling      | Automatic                    |
| Frequency    | Once per object              |
| Access       | Usually public               |

### Example

```cpp
class Student {
public:
    Student() {
        rollNo = 0;
        name = "";
        GPA = 0.0;
    }
};
```

---

## Default Constructor

- Takes no parameters  
- Compiler generates it if none is defined  
- Initializes members with default values  

| Data Type   | Default Value   |
|-------------|-----------------|
| int, float  | 0 / 0.0         |
| pointer     | nullptr / NULL  |

---

## Constructor Overloading

Multiple constructors with different parameter lists.

### Example

```cpp
class Student {
public:
    Student();
    Student(char *aName);
    Student(char *aName, int aRollNo);
    Student(char *aName, int aRollNo, float aGPA);
};
```


---

## Default Parameters in Constructor

Instead of multiple constructors:

### Example

```cpp
class Student {
public:
    Student(char *aName = NULL, int aRollNo = 0, float aGPA = 0.0) {
        name = aName;
        rollNo = aRollNo;
        GPA = aGPA;
    }
};
```

---

## Copy Constructor

Used to initialize one object from another.

### When it is called

- Object initialization from another object  
- Passing object by value  
- Returning object by value  

### Example

```cpp
Student studentB = studentA;  // Copy constructor
```

---

## Shallow Copy vs Deep Copy

### Shallow Copy

- Default compiler behavior  
- Copies values directly  
- Pointer copies only address → shared memory issue  

### Deep Copy

- Allocates new memory  
- Copies actual data  
- Prevents shared memory problems  

### Deep Copy Example

```cpp
Student::Student(const Student &obj) {
    rollNo = obj.rollNo;
    GPA = obj.GPA;

    int len = strlen(obj.name);
    name = new char[len + 1];
    strcpy(name, obj.name);
}
```

---

## Constructor vs other Methods (Important Difference)

| Feature             | Constructor                      | Method         |
|--------------------|----------------------------------|---------------------------------|
| Purpose            | Initialize object                | Perform operations              |
| Name               | Same as class                    | Any valid name                  |
| Return Type        | No return type                   | Must have return type           |
| Call Time          | Automatic at object creation     | Called explicitly               |
| Frequency          | Once per object                  | Multiple times                  |
| Inheritance        | Not inherited                    | Inherited                       |
| Overloading        | Allowed                          | Allowed                         |
| Object Requirement | Not required to call explicitly  | Requires object                 |

---

## Summary

| Concept                 | Purpose                      |
|-------------------------|------------------------------|
| Properties              | Store object state           |
| Methods                 | Define behavior              |
| Constructors            | Initialize objects           |
| Constructor Overloading | Multiple initialization ways |
| Copy Constructor        | Object duplication           |
| Deep Copy               | Safe memory handling         |

---
