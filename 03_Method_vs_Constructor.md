
# 🔹 Difference Between Method/Function and Constructor

|                       | **Method/Function**                                | **Constructor**                                          |
| --------------------- | -------------------------------------------------- | -------------------------------------------------------- |
| **Purpose**           | Performs an action or operation                    | Initializes an object when created                       |
| **Name**              | Can have any name                                  | Must have the same name as the class                     |
| **Return Type**       | Has a return type (`void`, `int`, `string`, etc.)  | No return type (not even `void`)                         |
| **Call Time**         | Called explicitly (manually)                       | Called automatically when object is created              |
| **Calling Syntax**    | `object.methodName();`                             | `ClassName objectName();`                                |
| **Frequency**         | Can be called multiple times                       | Called only once per object                              |

---

## 🔹 Example

```cpp
class Student {
public:
    string name;
    
    // Constructor
    Student(string n) {
        name = n;
    }
    
    // Method
    void display() {
        cout << name << endl;
    }
};

int main() {
    Student s1("Ali");    // Constructor called automatically
    
    s1.display();         // Method called manually
    
    return 0;
}
```

---

🔹 Quick Summary

 Constructor Method
When called? Automatically Manually
How many times? Once Many times
Name? Same as class Any name
Return type? No Yes

---

Member Functions

· Member functions are methods/functions that operate on data encapsulated in a class.
· Public member functions act as the interface of the class.

---

Defining Member Functions

Member functions can be defined in two ways:

1. Inside Class Definition

```cpp
class ClassName {
public:
    ReturnType FunctionName() {
        // code
    }
};
```

Example:

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

2. Outside Class Definition

Must be declared inside class first.

Syntax:

```cpp
class ClassName {
public:
    ReturnType FunctionName();
};

ReturnType ClassName::FunctionName() {
    // code
}
```

Example:

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

Inline Functions

· Compiler replaces function call with function code.
· inline keyword is used (request, not a command).
· Functions defined inside class are inline by default.

Example:

```cpp
inline int Area(int len, int hi) {
    return len * hi;
}
```

Inline with Class:

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

Constructors

· Used to initialize objects.
· Ensures object is in valid state at creation.
· Automatically called when object is created.
· Same name as class.
· No return type.
· Usually public.

Example:

```cpp
class Student {
public:
    Student() {
        rollNo = 0;
    }
};
```

Usage:

```cpp
int main() {
    Student s1; // constructor called automatically
}
```

---

Default Constructor

· Constructor with no arguments.
· Compiler generates one if not defined.
· Initializes members to default values.

Example:

```cpp
class Student {
    int rollNo;
    char *name;
    float GPA;
};
```

Compiler generated:

```
rollNo = 0;
GPA = 0.0;
name = NULL;
```

---

Constructor Overloading

· Multiple constructors with different parameters.
· Used for flexible initialization.

Example:

```cpp
class Student {
public:
    Student();
    Student(char *aName);
    Student(char *aName, int aRollNo);
    Student(char *aName, int aRollNo, float aGPA);
};
```

Example with Logic:

```cpp
Student::Student(int aRollNo, char *aName) {
    if (aRollNo < 0)
        rollNo = 0;
    else
        rollNo = aRollNo;
}
```

---

Usage:

```cpp
int main() {
    Student s1;
    Student s2("Name");
    Student s3("Name", 1);
    Student s4("Name", 1, 4.0);
}
```

---

Default Parameters in Constructor

```cpp
Student::Student(char *aName = NULL,
                 int aRollNo = 0,
                 float aGPA = 0.0) {
}
```

Equivalent to multiple constructors.

---

Copy Constructor

Used when:

· Object is initialized at creation
· Object is passed by value

Example:

```cpp
void func1(Student student) {
}

int main() {
    Student studentA;
    Student studentB = studentA;
    func1(studentA);
}
```

---

Syntax:

```cpp
Student::Student(const Student &obj) {
    rollNo = obj.rollNo;
    name = obj.name;
    GPA = obj.GPA;
}
```

---

Shallow Copy

· Default copying mechanism.
· Copies values directly.
· May cause shared memory issues.

---

Deep Copy (Custom Copy Constructor)

```cpp
Student::Student(const Student &obj) {
    int len = strlen(obj.name);
    name = new char[len + 1];
    strcpy(name, obj.name);

    rollNo = obj.rollNo;
    GPA = obj.GPA;
}
```

---

Summary

· Member functions define behavior of class.
· Constructors initialize objects automatically.
· Overloading provides flexibility.
· Copy constructor handles object copying.
· Deep copy prevents shared memory issues.

```
