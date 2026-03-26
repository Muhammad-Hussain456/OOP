# 🔹 Difference Between Method and Constructor

|       | **Method / Function** | **Constructor** |
|-------|----------------------|-----------------|
| **Purpose** | Performs an action or operation | Initializes an object when created |
| **Name** | Can have any name | Must have the same name as the class |
| **Return Type** | Has a return type (void, int, string, etc.) | No return type (not even void) |
| **Call Time** | Called explicitly (manually) | Called automatically when object is created |
| **Calling Syntax** | `object.methodName();` | `ClassName objectName();` |
| **Frequency** | Can be called multiple times | Called only once per object |

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

## 🔹 Quick Summary

| | **Constructor** | **Method** |
|---|----------------|-----------|
| When called? | Automatically | Manually |
| How many times? | Once | Many times |
| Name? | Same as class | Any name |
| Return type? | No | Yes |
