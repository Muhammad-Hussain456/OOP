# Class Structure: Properties and Methods (C++)

---

## Class Structure Overview

A class in Object-Oriented Programming (OOP) is composed of two main components:

| Component  | Also Known As                    | Purpose                           |
|------------|----------------------------------|-----------------------------------|
| Properties | Attributes, Data Members, Fields | Store the state/data of an object |
| Methods    | Member Functions, Behaviors      | Define actions an object can perform |

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

Member functions are functions defined inside a class that operate on its data members.

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

## Inline Functions

### Key Points

- Compiler replaces function call with actual code  
- `inline` is a request, not a command  
- Functions defined inside class are automatically inline  

### Example

```cpp
inline int Area(int len, int hi) {
    return len * hi;
}
```

Inside class:

```cpp
class Student {
    int rollNo;
public:
    void setRollNo(int aRollNo) {  // implicitly inline
        rollNo = aRollNo;
    }
};
```

---

## Constructors

Constructors are special member functions used to initialize objects automatically at creation.

### Characteristics

| Feature      | Description                  |
|--------------|------------------------------|
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

```cpp
class Student {
public:
    Student();
    Student(char *aName);
    Student(char *aName, int aRollNo);
    Student(char *aName, int aRollNo, float aGPA);
};
```

### Example Implementation

```cpp
Student::Student(char *aName, int aRollNo) {
    name = aName;
    if (aRollNo < 0)
        rollNo = 0;
    else
        rollNo = aRollNo;
}
```

---

## Default Parameters in Constructor

Instead of multiple constructors:

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

## Constructor vs Methods (Important Difference)

| Feature             | Constructor                      | Method (Member Function)        |
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
