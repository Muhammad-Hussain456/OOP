# 🔹 Abstraction

## What is Abstraction?

**Abstraction** is a fundamental concept of Object-Oriented Programming (OOP) that focuses on showing only essential features of an object while hiding unnecessary implementation details.

👉 **Abstraction = Show Essential Features + Hide Implementation Details**

Abstraction helps developers manage complexity by focusing only on what is important.

---

## 🔹 Abstraction in Programming

Abstraction is a way to cope with complexity in programming. It allows us to focus on the essential features of an object while hiding unnecessary details.

### Real-World Example

When you drive a car:

**You use (Essential Features):**
- Steering wheel
- Accelerator pedal
- Brake pedal

**You do not need to know (Hidden Details):**
- Engine working mechanism
- Fuel injection system
- Internal wiring
- Cooling system

This is **abstraction** — you interact with a simplified interface while the complex implementation remains hidden.

---

## 🔹 Principle of Abstraction

The principle of abstraction can be summarized as:

> **"Capture only those details about an object that are relevant to the current perspective."**

This means:
- Same object can be viewed differently
- Different perspectives require different abstractions
- Details irrelevant to current context are hidden

---

## 🔹 Example of Abstraction

A **Person** can be viewed differently depending on perspective:

| Perspective | Relevant Attributes (Shown) | Hidden Attributes |
|-------------|----------------------------|-------------------|
| **Student** | Roll number, grades, courses | Salary, department |
| **Teacher** | Subjects taught, department, salary | Grades, courses taken |
| **Employee** | Employee ID, department, salary | Grades, subjects |

Each view:
- Shows **relevant details** for that perspective
- Hides **irrelevant details** for that perspective

This is abstraction in action.

---

## 🔹 Visual Representation

```
                    ┌─────────────────┐
                    │     Person      │
                    │   (Abstract)    │
                    └────────┬────────┘
                             │
         ┌───────────────────┼───────────────────┐
         ▼                   ▼                   ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│    Student      │ │    Teacher      │ │    Employee     │
├─────────────────┤ ├─────────────────┤ ├─────────────────┤
│ - rollNo        │ │ - subjects      │ │ - employeeID    │
│ - grades        │ │ - department    │ │ - department    │
│ - courses       │ │ - salary        │ │ - salary        │
└─────────────────┘ └─────────────────┘ └─────────────────┘

Each subclass shows only relevant attributes
```

---

## 🔹 Levels of Abstraction

Abstraction exists at two levels:

| Level | Description | Example |
|-------|-------------|---------|
| **Design Level** | Focus on essential features and relationships | UML diagrams, architecture design |
| **Implementation Level** | Hide implementation details in code | Abstract classes, interfaces |

---

## 🔹 Ways to Achieve Abstraction

Abstraction can be achieved using:

1. **Abstract Classes** — Classes that cannot be instantiated
2. **Interfaces** — Contracts that define what to do, not how to do it

---

## 🔹 Abstract Class

### What is an Abstract Class?

An **abstract class** is a class that cannot be instantiated and is used to define abstraction. It serves as a blueprint for other classes.

### Characteristics

| Characteristic | Description |
|----------------|-------------|
| **Cannot be instantiated** | No objects can be created directly |
| **Can contain abstract methods** | Methods without implementation |
| **Can contain concrete methods** | Methods with full implementation |
| **Can have data members** | Can store state (variables) |
| **Used as base class** | Designed to be inherited from |
| **Supports inheritance** | Derived classes extend it |

### UML Representation

```
┌─────────────────────────────────────┐
│           Vehicle                   │
│           <<abstract>>              │
├─────────────────────────────────────┤
│ + start() : void (abstract)         │
│ + stop() : void (abstract)          │
│ + accelerate() : void (concrete)    │
└─────────────────────────────────────┘
              △
              │ (Inheritance)
    ┌─────────┴─────────┐
    ▼                   ▼
┌───────────┐     ┌───────────┐
│   Car     │     │   Bike    │
├───────────┤     ├───────────┤
│ + start() │     │ + start() │
│ + stop()  │     │ + stop()  │
└───────────┘     └───────────┘
```

### Abstract Method (Pure Virtual Function)

An **abstract method** (pure virtual function in C++):
- Has **no implementation** in the abstract class
- Must be **implemented** in derived classes
- Ends with `= 0` in C++

```cpp
virtual void start() = 0;  // Abstract method
```

---

## 🔹 Interface

### What is an Interface?

An **interface** is a contract that defines **what** a class must do, without specifying **how** it should do it. In C++, interfaces are implemented using **pure abstract classes** (classes with only pure virtual functions).

### Characteristics

| Characteristic | Description |
|----------------|-------------|
| **Cannot be instantiated** | No objects can be created |
| **Contains only abstract methods** | No implementation in interface |
| **No data members** | Typically no state/variables |
| **All methods are public** | Interface defines public contract |
| **Multiple inheritance allowed** | A class can implement multiple interfaces |

### Interface vs Abstract Class

| Feature | Interface | Abstract Class |
|---------|-----------|----------------|
| **Methods** | Only abstract methods | Can have both abstract and concrete methods |
| **Data Members** | No data members | Can have data members |
| **Access Modifiers** | All methods public | Can have protected, private members |
| **Multiple Inheritance** | Supported (class can implement multiple interfaces) | Limited (single inheritance in C++) |
| **Purpose** | Define contract/behavior | Define common base with shared code |
| **Implementation** | "What" to do | "What" and partial "how" |

### Interface in C++ (Pure Abstract Class)

```cpp
// Interface (Pure Abstract Class)
class Drawable {
public:
    virtual void draw() = 0;
    virtual void setColor(string color) = 0;
    virtual ~Drawable() {}  // Virtual destructor
};

// Another Interface
class Serializable {
public:
    virtual void save() = 0;
    virtual void load() = 0;
    virtual ~Serializable() {}
};

// Class implementing multiple interfaces
class Circle : public Drawable, public Serializable {
private:
    string color;
    float radius;
    
public:
    void draw() override {
        cout << "Drawing circle" << endl;
    }
    
    void setColor(string c) override {
        color = c;
    }
    
    void save() override {
        cout << "Saving circle" << endl;
    }
    
    void load() override {
        cout << "Loading circle" << endl;
    }
};
```

### Benefits of Interfaces

1. **Separation of Concerns**: Separates specification from implementation
2. **Loose Coupling**: Classes depend on interfaces, not concrete implementations
3. **Multiple Inheritance**: Allows a class to exhibit multiple behaviors
4. **Testability**: Easy to mock interfaces for unit testing
5. **Flexibility**: Implementation can change without affecting users

---

## 🔹 Real-World Examples of Abstraction

| Real World Object | Abstraction (What User Sees) | Hidden Complexity |
|-------------------|------------------------------|-------------------|
| **ATM Machine** | Withdraw, Deposit, Check Balance | Banking system, network communication, security protocols |
| **Car** | Drive, Brake, Accelerate | Engine, transmission, fuel injection, cooling system |
| **Mobile Phone** | Call, Message, Camera, Apps | Operating system, processor, memory management, network protocols |
| **TV Remote** | Power, Volume, Channel | Infrared signals, encoding, device pairing |
| **Coffee Machine** | Press button, get coffee | Heating, pressure, grinding, water flow |

User interacts with **interface only**, not with the **implementation**.

---

## 🔹 Advantages of Abstraction

### 1. Simplifies Model
Only important features are shown to the user, making complex systems easier to understand.

### 2. Reduces Complexity
Users don't need to understand internal working to use the system effectively.

### 3. Provides Flexibility
Implementation can change without affecting users as long as the interface remains the same.

### 4. Improves Code Reusability
Abstract classes and interfaces can be reused across different parts of the application.

### 5. Improves Maintainability
Changes inside the class do not affect outside code, making maintenance easier.

### 6. Enhances Security
Implementation details are hidden, preventing misuse or accidental modification.

---

## 🔹 Encapsulation vs Abstraction

| Feature | Encapsulation | Abstraction |
|---------|---------------|-------------|
| **Purpose** | Hide data | Hide complexity |
| **Focus** | Data security and integrity | Essential features |
| **Implementation** | Access modifiers (private, public) | Abstract classes, interfaces |
| **What it hides** | Data members (state) | Implementation details |
| **Example** | Private variables with getters/setters | Abstract class Vehicle with start() method |
| **Level** | Implementation level | Both design and implementation level |

### Visual Difference

```
ENCAPSULATION                          ABSTRACTION
┌─────────────────┐                   ┌─────────────────┐
│     Class       │                   │   Interface     │
│  ┌───────────┐  │                   │                 │
│  │ Private   │  │  ← Data hidden    │   What to do    │
│  │ Data      │  │                   │   (Contract)    │
│  └───────────┘  │                   │                 │
│  ┌───────────┐  │                   │       ▲         │
│  │ Public    │  │  ← Controlled     │       │         │
│  │ Methods   │  │    access         │  ┌────┴────┐    │
│  └───────────┘  │                   │  │ How to  │    │
└─────────────────┘                   │  │ do it   │    │
                                      │  └─────────┘    │
Focus: HOW to hide data               │  Implementation │
                                      └─────────────────┘
                                      Focus: WHAT to do
```

---

## 🔹 Real-World Analogy

| Example | Abstraction in Action |
|---------|----------------------|
| **Car** | You drive using steering wheel, pedals — don't need to know engine mechanics |
| **ATM** | You withdraw cash using simple interface — don't need to know banking system |
| **Phone** | You use apps through touchscreen — don't need to know OS or hardware |
| **Restaurant** | You order from menu — don't need to know kitchen operations |
| **Airplane** | You board and sit — don't need to know flight systems |

---

## 🔹 Key Points to Remember

✅ Abstraction **hides implementation details**
✅ Shows only **essential features**
✅ **Reduces complexity** for users
✅ Implemented using **abstract classes** and **interfaces**
✅ **Abstract class** cannot be instantiated
✅ **Interface** defines contract (what to do)
✅ **Derived classes** implement abstract behavior
✅ Helps achieve **loose coupling** in software design
✅ **Different perspectives** require different abstractions

---

## 🔹 Summary

| Aspect | Description |
|--------|-------------|
| **Definition** | Show essential features, hide implementation |
| **Purpose** | Manage complexity, focus on what's important |
| **Implementation** | Abstract classes, interfaces |
| **Abstract Class** | Cannot instantiate, can have concrete methods |
| **Interface** | Pure contract, only abstract methods |
| **Benefits** | Simplicity, reusability, maintainability, flexibility |
| **Relation to Encapsulation** | Abstraction hides complexity; Encapsulation hides data |

**Abstraction** is the foundation of good software design — it allows us to build complex systems by focusing on one level of detail at a time, hiding unnecessary complexity from each layer of the application.

---

## 🔹 Quick Reference

### When to Use Abstract Class vs Interface

| Scenario | Use Abstract Class | Use Interface |
|----------|-------------------|---------------|
| Need shared code | ✓ | ✗ |
| Need to define state | ✓ | ✗ |
| Need multiple inheritance | ✗ | ✓ |
| Need to define contract only | ✗ | ✓ |
| Classes are closely related | ✓ | ✗ |
| Unrelated classes share behavior | ✗ | ✓ |

### C++ Implementation Summary

| Concept | C++ Syntax |
|---------|------------|
| Abstract Method | `virtual void method() = 0;` |
| Abstract Class | Class with at least one pure virtual function |
| Interface | Class with all pure virtual functions |
| Override | `void method() override { }` |
| Virtual Destructor | `virtual ~ClassName() {}` |
