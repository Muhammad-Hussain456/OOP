# 🔹 Polymorphism

## What is Polymorphism?

**Polymorphism** is a fundamental concept of Object-Oriented Programming (OOP) that allows objects of different classes to be treated as objects of a common base class, with each responding to the same message in its own way.

👉 **Polymorphism = Many Forms + One Interface + Multiple Implementations**

The word "polymorphism" comes from Greek:
- **Poly** = Many
- **Morph** = Forms

---

## 🔹 Real-World Analogies

### Analogy 1: Sound Button
A **sound button** in a mobile game:
- Press the button → Dog barks 🐕
- Press the button → Cat meows 🐈
- Press the button → Cow moos 🐄

**Same interface** (press button), **different behaviors** (different sounds)

---

### Analogy 2: Shapes
A **draw()** command:
- For Circle → Draws a circle
- For Rectangle → Draws a rectangle
- For Triangle → Draws a triangle

**Same command** (draw), **different visual outputs** (based on shape)

---


## 🔹 Examples of Polymorphism 

### Example 1: Vehicle System
A transportation system has different vehicles:
- **Car** → Start with key ignition, accelerate smoothly
- **Bike** → Start with kick start, accelerate quickly
- **Truck** → Start with heavy engine, accelerate slowly

All vehicles have the same interface: `start()` and `accelerate()`. But each vehicle **responds differently** to these commands based on its type.

---

### Example 2: Employee Management
An HR system processes different types of employees:
- **Manager** → Calculate bonus: 20% of salary
- **Developer** → Calculate bonus: 15% of salary
- **Intern** → Calculate bonus: 5% of salary

The HR system uses the same `calculateBonus()` method for all employees, but each employee type **calculates differently**.

---

### Example 5: Database Operations
A database system supports different database types:
- **MySQL** → Execute MySQL-specific query syntax
- **PostgreSQL** → Execute PostgreSQL-specific query syntax
- **MongoDB** → Execute NoSQL query syntax

The application uses the same `query(sql)` interface, but each database **processes queries in its own way**.

---

## 🔹 Types of Polymorphism

Polymorphism in OOP is classified into two main types:

| Type | Description | When It's Determined |
|------|-------------|---------------------|
| **Compile-time Polymorphism** | Behavior determined during compilation | At compile time |
| **Run-time Polymorphism** | Behavior determined during program execution | At runtime |

---

## 🔹 Part 1: Compile-time Polymorphism (Static Polymorphism)

### Definition
Compile-time polymorphism occurs when the compiler determines which method or operation to execute **during compilation**, before the program runs.

### How It Works
The compiler decides based on:
- Number of parameters
- Type of parameters
- Order of parameters

### Ways to Achieve

#### 1️⃣ Function Overloading
Multiple functions with the **same name** but **different parameters** in the same scope.

**Real-world analogy**: A person named "John" who does different things:
- John → Fixes cars (mechanic)
- John → Treats patients (doctor)
- John → Teaches students (teacher)

Same name, different roles based on context.

---

#### 2️⃣ Operator Overloading
Redefining the behavior of operators (+, -, *, etc.) for user-defined types.

**Real-world analogy**: The plus sign (+) meaning different things:
- 5 + 3 → Adds numbers (result: 8)
- "Hello" + "World" → Concatenates strings (result: "HelloWorld")
- 2 hours + 3 hours → Adds time durations (result: 5 hours)

Same operator, different meanings based on what it operates on.

---

### Characteristics of Compile-time Polymorphism

| Characteristic | Description |
|----------------|-------------|
| **Early Binding** | Method call resolved at compile time |
| **Faster Execution** | No runtime overhead for method resolution |
| **Less Flexible** | Behavior fixed at compile time |
| **Predictable** | Compiler knows exactly which method to call |

---

## 🔹 Part 2: Run-time Polymorphism (Dynamic Polymorphism)

### Definition
Run-time polymorphism occurs when the program determines which method to execute **during execution**, based on the actual object type.

### How It Works
The decision is made at runtime based on:
- Actual object type (not reference/pointer type)
- Inheritance hierarchy
- Method overriding

### Way to Achieve
**Method Overriding**

#### Method Overriding
When a derived class provides its own implementation of a method that is already defined in its base class.

**Real-world analogy**: A family of animals responding to "makeSound":
- Animal (general) → Makes a generic sound
- Dog (specific) → Barks
- Cat (specific) → Meows

The same command `makeSound()` produces different results based on the actual animal.

---

### Characteristics of Run-time Polymorphism

| Characteristic | Description |
|----------------|-------------|
| **Late Binding** | Method call resolved at runtime |
| **Slower Execution** | Slight overhead for dynamic resolution |
| **More Flexible** | Behavior can vary at runtime |
| **Extensible** | New types can be added without modifying existing code |

---

## 🔹 Method Overriding in Multiple Inheritance

In inheritance, we may come across situations where a **child class inherits the same method from two parent classes**. This creates **ambiguity** — the compiler doesn't know which version of the method to use.

### The Problem: Ambiguous Inheritance

When a child class inherits from two parent classes, and both parents have a method with the same name and signature, the child inherits **two versions** of the same method. This creates confusion about which method should be called.

### Real-world Analogy
A **multi-function device** (printer + scanner):
- Printer has a `start()` method (starts printing)
- Scanner has a `start()` method (starts scanning)

When the multi-function device inherits both, which `start()` should it use?

### The Solution: Method Overriding

**Method overriding** resolves this ambiguity by:
1. **Explicitly overriding** the conflicting method in the child class
2. **Defining which behavior** the child should exhibit
3. **Optionally combining** or selecting from parent implementations

The child class provides its **own implementation**, which may:
- Call one parent's version
- Call both parents' versions
- Provide entirely new behavior


---

## 🔹 Overriding vs Overloading

| Feature | Overriding | Overloading |
|---------|------------|-------------|
| **Definition** | Redefining a base class method in derived class | Multiple functions with same name, different parameters |
| **Scope** | Different classes (inheritance hierarchy) | Same class or scope |
| **Parameters** | Must be identical | Must be different |
| **Binding** | Runtime (dynamic) | Compile-time (static) |
| **Polymorphism Type** | Run-time polymorphism | Compile-time polymorphism |
| **Inheritance Required** | Yes | No |

---

## 🔹 Advantages of Polymorphism

### 1. Code Reusability
Write code that works with base class; it automatically works with all derived classes without modification.

### 2. Flexibility
Add new derived classes without modifying existing code that uses the base class interface.

### 3. Maintainability
Changes in derived classes don't affect code that uses base class interface.

### 4. Extensibility
Easy to add new types that respond to existing interfaces.

### 5. Simplified Code
Single interface for multiple implementations reduces complexity.

### 6. Resolves Inheritance Conflicts
Method overriding provides a clean way to resolve ambiguous method inheritance in multiple inheritance scenarios.

---

## 🔹 Key Points to Remember

✅ **Polymorphism** means "many forms" — same interface, different implementations

✅ **Compile-time polymorphism**: Function overloading, operator overloading — resolved at compile time

✅ **Run-time polymorphism**: Method overriding with virtual functions — resolved at runtime

✅ **Method overriding** allows derived classes to provide specific implementations

✅ **Multiple inheritance conflicts** (ambiguous methods) are resolved through method overriding

✅ **Abstract classes** define interfaces that derived classes must implement

✅ **Overloading** is compile-time; **Overriding** is runtime

---

## 🔹 Summary Table

| Aspect | Compile-time Polymorphism | Run-time Polymorphism |
|--------|--------------------------|----------------------|
| **Also Known As** | Static polymorphism | Dynamic polymorphism |
| **Implementation** | Function overloading, Operator overloading | Method overriding|
| **Binding** | Early binding (compile-time) | Late binding (run-time) |
| **Speed** | Faster | Slightly slower |
| **Flexibility** | Less flexible | More flexible |
| **Inheritance Required** | No | Yes |
| **Resolves Multiple Inheritance Conflicts** | N/A | Yes |
