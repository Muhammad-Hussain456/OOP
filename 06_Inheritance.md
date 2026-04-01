# Inheritance

## What is Inheritance?

**Inheritance** is a mechanism where a derived class (child) inherits properties and behaviors from a base class (parent).  
Major benefit of inheritance is reuse.

👉 **Inheritance = Code Reusability + Hierarchical Classification + IS-A Relationship**

---

## Base Class vs Derived Class

If a class B inherits from class A then it contains all the characteristics (information structure and behaviour) of class A.  
The **parent class** is called **base class** and the **child class** is called **derived class**.  
Derived class inherits all the characteristics of the base class.  
Besides inherited characteristics, derived class may have its own unique characteristics.

---

### Inheritance – “IS A” or “IS A KIND OF” Relationship

Each derived class is a special kind of its base class.

#### Example

```
        ┌─────────────────┐
        │     Person      │ 
        ├─────────────────┤
        │ - name          │
        │ - age           │
        │ - gender        │
        ├─────────────────┤
        │ + eat()         │
        │ + walk()        │
        └────────┬────────┘
                 │
    ┌────────────┼────────────┐
    ▼            ▼            ▼
┌─────────┐ ┌─────────┐  ┌────────┐
│Teacher  │ │Student  │  │Doctor  │
├─────────┤ ├─────────┤  ├────────┤
│-subject│ │-program │  │-special│
│-salary │ │-year    │  │-license│
├─────────┤ ├─────────┤  ├────────┤
│+teach()│ │+study() │  │+treat()│
└─────────┘ └─────────┘  └────────┘
```

---

## Key Benefits/Advantages

| Benefit | Description |
|---------|-------------|
| **Code Reusability** | Child classes automatically get parent's features |
| **Hierarchical Organization** | Natural classification of related concepts |
| **Extensibility** | Add new features without modifying existing code |
| **Polymorphism Support** | Enables runtime polymorphism through method overriding (covered later) |

---

### Reuse with Inheritance

Main purpose of inheritance is reuse.  
We can easily add new classes by inheriting from existing classes.  
Select an existing class closer to the desired functionality.  
Create a new class and inherit it from the selected class.  
Add to and/or modify the inherited functionality.

#### Example

```
        ┌─────────────────┐
        │     Shape       │  ← Generalized base class
        ├─────────────────┤
        │ - color         │
        │ - vertices      │
        ├─────────────────┤
        │ + move()        │
        │ + setColor()    │
        └────────┬────────┘
                 │
    ┌────────────┼────────────┐
    ▼            ▼            ▼
┌───────┐  ┌───────┐    ┌─────────┐
│ Circle│  │ Line  │    │ Triangle│
├───────┤  ├───────┤    ├─────────┤
│-radius│  │-length│    │-angle   │
├───────┤  ├───────┤    ├─────────┤
│+area()│  │+length│    │+area()  │
└───────┘  └───────┘    └─────────┘
```

---

# Concepts Related to Inheritance

The following concepts are closely related to inheritance:

1. **Generalization**
2. **Sub-typing (Extension)**
3. **Specialization (Restriction)**
4. **Abstract Classes**
5. **Concrete Classes**

---

## Generalization

### Definition
**Generalization** is the process of extracting common characteristics from multiple classes and creating a new base class.

### Explanation
In OO models, some classes may have common characteristics.  
We extract these features into a new class and inherit original classes from this new class.  
This concept is known as Generalization.

### Purpose
- Reduce redundancy
- Improve maintainability
- Promote reuse

### Direction
**Bottom-up** process: From specific classes to general base class.

### Visual Representation

**Before Generalization:**
```
┌─────────────┐  ┌─────────────┐  ┌─────────────┐
│   Circle    │  │    Line     │  │  Triangle   │
├─────────────┤  ├─────────────┤  ├─────────────┤
│ - color     │  │ - color     │  │ - color     │
│ - vertices  │  │ - vertices  │  │ - vertices  │
│ - radius    │  │ - length    │  │ - angle     │
│ - move()    │  │ - move()    │  │ - move()    │
│ - setColor()│  │ - setColor()│  │ - setColor()│
│ - area()    │  │ - getLength()│  │ - area()    │
└─────────────┘  └─────────────┘  └─────────────┘
```

**After Generalization:**
```
        ┌─────────────────┐
        │     Shape       │  ← Generalized base class
        ├─────────────────┤
        │ - color         │
        │ - vertices      │
        ├─────────────────┤
        │ + move()        │
        │ + setColor()    │
        └────────┬────────┘
                 │
    ┌────────────┼────────────┐
    ▼            ▼            ▼
┌───────┐  ┌───────┐    ┌─────────┐
│ Circle│  │ Line  │    │ Triangle│
├───────┤  ├───────┤    ├─────────┤
│-radius│  │-length│    │-angle   │
├───────┤  ├───────┤    ├─────────┤
│+area()│  │+length│    │+area()  │
└───────┘  └───────┘    └─────────┘
```

### Example: Person Hierarchy

**Before Generalization:**
```
Teacher, Student, Doctor classes each contain:
- name, age, gender
- eat(), walk()
```

**After Generalization:**
```
        ┌─────────────────┐
        │     Person      │  ← Generalized base class
        ├─────────────────┤
        │ - name          │
        │ - age           │
        │ - gender        │
        ├─────────────────┤
        │ + eat()         │
        │ + walk()        │
        └────────┬────────┘
                 │
    ┌────────────┼────────────┐
    ▼            ▼            ▼
┌─────────┐ ┌─────────┐  ┌────────┐
│Teacher  │ │Student  │  │Doctor  │
├─────────┤ ├─────────┤  ├────────┤
│-subject│ │-program │  │-special│
│-salary │ │-year    │  │-license│
├─────────┤ ├─────────┤  ├────────┤
│+teach()│ │+study() │  │+treat()│
└─────────┘ └─────────┘  └────────┘
```

---

## Sub-typing (Extension)

### Definition
**Sub-typing** occurs when a derived class **extends** the behavior of a base class without violating base class expectations.

### Explanation
We want to add a new class to an existing model.  
Find an existing class that already implements some of the desired state and behaviour.  
Inherit the new class from this class and add unique behaviour to the new class.

### Key Concept
Derived class is **behaviorally compatible** with base class.

### Behavioral Compatibility
Behaviourally compatible means that **base class** can be replaced by the **derived class** (Liskov Substitution Principle).

### Characteristics
- Adds new methods and properties
- Preserves all base class contracts
- Maintains behavioral compatibility
- Follows "IS-A" relationship strictly

### Example: Student extends Person

| Person (Base) | Student (Derived) |
|---------------|-------------------|
| name | name (inherited) |
| age | age (inherited) |
| gender | gender (inherited) |
| eat() | eat() (inherited) |
| walk() | walk() (inherited) |
| | **program** (new) |
| | **studyYear** (new) |
| | **study()** (new) |
| | **takeExam()** (new) |

---

## Specialization (Restriction)

### Definition
**Specialization** occurs when a derived class **restricts** behavior of base class by adding constraints.

### Key Concept
Derived class may be **behaviorally incompatible** with base class in some aspects.

### Behavioral Incompatibility
Base class **cannot always** be replaced by derived class due to restrictions.

### Characteristics
- Adds validation or constraints
- May override methods with stricter rules
- May violate Liskov Substitution Principle
- Represents a more specific subset

### Example: Adult restricts Person

| Person (Base) | Adult (Derived) |
|---------------|-----------------|
| age: 0-100 | age: 18-100 (restricted) |
| setAge(15) ✓ allowed | setAge(15) ✗ rejected |

### Example: NaturalSet restricts IntegerSet

| IntegerSet (Base) | NaturalSet (Derived) |
|-------------------|---------------------|
| add(-5) ✓ allowed | add(-5) ✗ rejected |
| add(0) ✓ allowed | add(0) ✗ rejected |
| add(10) ✓ allowed | add(10) ✓ allowed |

---

## Abstract Classes

### Definition
An **abstract class** represents an **abstract concept** that cannot be instantiated directly.

👉 **Abstract Class = Blueprint + Contract + Common Implementation**

### Explanation
An abstract class implements an abstract concept.  
Main purpose is to be inherited by other classes.  
Can’t be instantiated.  
Promotes reuse.

### Characteristics

| Characteristic | Description |
|----------------|-------------|
| **Cannot be instantiated** | No objects can be created |
| **Contains abstract methods** | Methods without implementation |
| **Used as base class** | Designed for inheritance |
| **May contain concrete methods** | Common implementation for children |
| **Defines interface** | Contract for derived classes |

### Role in Inheritance
Abstract classes serve a crucial role in inheritance hierarchies:

1. **Provide Common Interface**: Define what derived classes must implement
2. **Share Common Code**: Provide concrete methods that all children can use
3. **Enable Polymorphism**: Base class pointers can refer to derived objects
4. **Prevent Instantiation**: Ensures only concrete classes are instantiated

### Example: Vehicle Hierarchy

```
┌─────────────────────────────────────────────┐
│         Vehicle (Abstract)                  │
├─────────────────────────────────────────────┤
│ Properties: brand, model, speed             │
├─────────────────────────────────────────────┤
│ Concrete Methods:                           │
│   + accelerate()   ← Shared by all vehicles │
│   + applyBrakes()  ← Shared by all vehicles │
├─────────────────────────────────────────────┤
│ Abstract Methods (must be implemented):     │
│   + start()        ← Each vehicle differs   │
│   + stop()         ← Each vehicle differs   │
│   + honk()         ← Each vehicle differs   │
└─────────────────────────────────────────────┘
                          △
                          │ (Inheritance)
          ┌───────────────┼───────────────┐
          │               │               │
┌─────────┴────────┐ ┌────┴──────┐ ┌─────┴──────┐
│   Car (Concrete) │ │Bike (Concrete)│Truck(Concrete)│
├──────────────────┤ ├───────────────┤ ├──────────────┤
│ + start()        │ │ + start()     │ │ + start()    │
│ + stop()         │ │ + stop()      │ │ + stop()     │
│ + honk()         │ │ + honk()      │ │ + honk()     │
└──────────────────┘ └───────────────┘ └──────────────┘
```

### Why Abstract Classes Cannot Be Instantiated

Abstract classes represent **incomplete concepts**:
- `Vehicle` is too generic - you can't have just a "vehicle"
- `Shape` is abstract - you need a specific shape
- `Person` is abstract - you need a student, teacher, etc.

---

## Concrete Classes

### Definition
A **concrete class** represents a **real-world object** that can be instantiated.

👉 **Concrete Class = Complete Implementation + Instantiable Objects**

### Explanation
A concrete class implements a concrete concept.  
Main purpose is to be instantiated.  
Provides implementation details specific to the domain context.

### Characteristics

| Characteristic | Description |
|----------------|-------------|
| **Can be instantiated** | Objects can be created |
| **Provides full implementation** | All methods have bodies |
| **Inherits from abstract classes** | Implements all abstract methods |
| **Domain specific** | Represents actual entities |

### Example: Person Hierarchy

```
┌─────────────────────────────────────┐
│      Person (Abstract)              │  ← Cannot instantiate
│      - name, age, gender            │
│      + eat(), walk()                │
│      + work() = 0 (abstract)        │
└─────────────────────────────────────┘
                △
                │ (Inheritance)
    ┌───────────┼───────────┐
    │           │           │
┌───┴────┐ ┌───┴────┐ ┌───┴────┐
│Student │ │Teacher │ │ Doctor │  ← Can instantiate
│(Concrete)│(Concrete)│(Concrete)│
├────────┤ ├────────┤ ├────────┤
│+ work()│ │+ work()│ │+ work()│
└────────┘ └────────┘ └────────┘
```

### Concrete Classes Complete the Abstraction

| Abstract Class | Concrete Classes |
|----------------|------------------|
| Shape | Circle, Rectangle, Triangle |
| Vehicle | Car, Bike, Truck |
| Person | Student, Teacher, Doctor |
| Animal | Dog, Cat, Bird |

---

# Comparison Table

## Generalization vs Specialization

| Aspect | Generalization | Specialization |
|--------|---------------|----------------|
| **Direction** | Bottom-up | Top-down |
| **Purpose** | Extract common features | Add specific features or constraints |
| **Result** | Creates base class | Creates derived class |
| **Behavior** | More general | More specific or restricted |
| **Example** | Extracting Shape from Circle, Line | Creating Adult with age restriction |

## Sub-typing vs Specialization

| Aspect | Sub-typing (Extension) | Specialization (Restriction) |
|--------|------------------------|------------------------------|
| **Behavior** | Extends base class | Restricts base class |
| **Compatibility** | Fully compatible | May be partially incompatible |
| **LSP** | Follows Liskov principle | May violate LSP |
| **New Features** | Adds new methods/properties | May only add constraints |
| **Example** | Student adds study() to Person | Adult restricts age range |

## Abstract Class vs Concrete Class

| Aspect | Abstract Class | Concrete Class |
|--------|---------------|----------------|
| **Instantiation** | Cannot be instantiated | Can be instantiated |
| **Purpose** | Define contract and common code | Represent actual objects |
| **Methods** | May have abstract methods | All methods implemented |
| **Role** | Base class in hierarchy | Leaf classes in hierarchy |
| **Example** | Vehicle | Car, Bike |

---

# Visual Summary

```
                    INHERITANCE CONCEPTS
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  GENERALIZATION (Bottom-up)                                     │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐                     │
│  │ Specific │  │ Specific │  │ Specific │                     │
│  │ Class 1  │  │ Class 2  │  │ Class 3  │                     │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘                     │
│       └─────────────┼─────────────┘                            │
│                     ▼                                           │
│            ┌─────────────────┐                                 │
│            │  Base Class     │  ← Extracts common features     │
│            │  (General)      │                                 │
│            └─────────────────┘                                 │
│                                                                 │
│  SPECIALIZATION (Top-down)                                      │
│            ┌─────────────────┐                                 │
│            │  Base Class     │                                 │
│            │  (General)      │                                 │
│            └────────┬────────┘                                 │
│       ┌─────────────┼─────────────┐                            │
│       ▼             ▼             ▼                            │
│ ┌──────────┐  ┌──────────┐  ┌──────────┐                     │
│ │Derived   │  │Derived   │  │Derived   │                     │
│ │Class 1   │  │Class 2   │  │Class 3   │                     │
│ │(Specific)│  │(Specific)│  │(Specific)│                     │
│ └──────────┘  └──────────┘  └──────────┘                     │
│       │             │             │                            │
│       └─────────────┼─────────────┘                            │
│                     ▼                                           │
│            ┌─────────────────┐                                 │
│            │ Sub-typing:     │  Extension (adds behavior)      │
│            │ Specialization: │  Restriction (adds constraints) │
│            └─────────────────┘                                 │
│                                                                 │
│  ABSTRACT vs CONCRETE                                           │
│  ┌─────────────────────────────────────┐                       │
│  │     ABSTRACT CLASS                  │                       │
│  │     (Cannot Instantiate)             │                       │
│  │  ┌───────────────────────────────┐  │                       │
│  │  │ + abstractMethod() = 0        │  │                       │
│  │  │ + concreteMethod() { }        │  │                       │
│  │  └───────────────────────────────┘  │                       │
│  └──────────────┬──────────────────────┘                       │
│                 │                                               │
│                 ▼ (Inheritance)                                 │
│  ┌─────────────────────────────────────┐                       │
│  │     CONCRETE CLASS                  │                       │
│  │     (Can Instantiate)                │                       │
│  │  ┌───────────────────────────────┐  │                       │
│  │  │ + abstractMethod() { }        │  │  ← Implements all     │
│  │  │ + concreteMethod() { }        │  │    abstract methods   │
│  │  └───────────────────────────────┘  │                       │
│  └─────────────────────────────────────┘                       │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

# Key Points to Remember

## Inheritance
- **IS-A relationship** between derived and base class
- Promotes **code reusability**
- Enables **polymorphism** (covered later)

## Generalization
- **Bottom-up** process
- Extracts **common features**
- Creates **base class** from multiple classes

## Sub-typing (Extension)
- Derived class **extends** base class behavior
- **Behaviorally compatible**
- Follows **Liskov Substitution Principle**
- Adds new capabilities without breaking existing ones

## Specialization (Restriction)
- Derived class **restricts** base class behavior
- May be **behaviorally incompatible**
- Adds **constraints or validation**
- Represents a more specific subset

## Abstract Class
- **Cannot be instantiated**
- Contains **abstract methods** (without implementation)
- Defines **contract** for derived classes
- May contain **concrete methods** for common functionality

## Concrete Class
- **Can be instantiated**
- Implements **all abstract methods**
- **Actual objects** are created using concrete class

---

# Common Interview Questions

### Q1: What's the difference between Generalization and Specialization?

**Generalization** extracts common features upward (bottom-up), while **Specialization** adds specific features or constraints downward (top-down).

### Q2: What is behavioral compatibility in Sub-typing?

Behavioral compatibility means a derived class object can replace a base class object without affecting program correctness (Liskov Substitution Principle).

### Q3: Why can't we instantiate (create object) an abstract class?

Abstract classes represent incomplete concepts. They contain abstract methods without implementation, so creating objects would leave functionality undefined.

### Q4: What's the relationship between Abstract and Concrete classes?

Concrete classes inherit from abstract classes and provide complete implementations of all abstract methods, making them instantiable.

---

# Summary Table

| Concept | Purpose | Direction | Key Feature | Example |
|---------|---------|-----------|-------------|---------|
| **Generalization** | Extract common features | Bottom-up | Creates base class | Shape from Circle, Line |
| **Sub-typing** | Extend behavior | Top-down | Full compatibility | Student extends Person |
| **Specialization** | Restrict behavior | Top-down | Adds constraints | Adult restricts age |
| **Abstract Class** | Define contract | N/A | Cannot instantiate | Vehicle class |
| **Concrete Class** | Create objects | N/A | Full implementation | Car class |
