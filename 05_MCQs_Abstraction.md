## Practice MCQs: Abstraction

---

Q1. Abstraction in OOP focuses on:

A) Showing all implementation details
B) Showing only essential features and hiding implementation details
C) Making all data public
D) Creating multiple objects

<details>
<summary>✅ Check Answer</summary>

Answer: B) Showing only essential features and hiding implementation details

💡 Abstraction = Show Essential Features + Hide Implementation Details

</details>

---

Q2. When you drive a car, which of the following represents abstraction?

A) Understanding the engine mechanism
B) Knowing the fuel injection system
C) Using the steering wheel and pedals
D) Studying internal wiring

<details>
<summary>✅ Check Answer</summary>

Answer: C) Using the steering wheel and pedals

💡 You use essential features (steering, pedals); complex internals are hidden.

</details>

---

Q3. The principle of abstraction can be summarized as:

A) Show everything about an object
B) Capture only details relevant to the current perspective
C) Hide all details including essential ones
D) Make all implementation visible

<details>
<summary>✅ Check Answer</summary>

Answer: B) Capture only details relevant to the current perspective

💡 Different perspectives require different abstractions.

</details>

---

Q4. A Person viewed as a Student shows roll number and grades. This is an example of:

A) Encapsulation
B) Polymorphism
C) Abstraction
D) Inheritance

<details>
<summary>✅ Check Answer</summary>

Answer: C) Abstraction

💡 Only student-relevant attributes shown; salary, department are hidden.

</details>

---

Q5. Which of the following is NOT a way to achieve abstraction in C++?

A) Abstract classes
B) Interfaces (pure abstract classes)
C) Global variables
D) Pure virtual functions

<details>
<summary>✅ Check Answer</summary>

Answer: C) Global variables

💡 Abstraction is achieved via abstract classes and interfaces.

</details>

---

Q6. An abstract class is a class that:

A) Can be instantiated directly
B) Cannot be instantiated
C) Contains only data members
D) Has no derived classes

<details>
<summary>✅ Check Answer</summary>

Answer: B) Cannot be instantiated

💡 Abstract class = cannot create objects directly; must be inherited.

</details>

---

Q7. Which of the following is true about an abstract class?

A) It can only contain abstract methods
B) It can contain both abstract and concrete methods
C) It cannot have data members
D) It cannot be inherited

<details>
<summary>✅ Check Answer</summary>

Answer: B) It can contain both abstract and concrete methods

💡 Abstract class = abstract methods + concrete methods + data members.

</details>

---

Q8. In C++, a pure virtual function is declared using:

A) virtual void func();
B) void func() = 0;
C) virtual void func() = 0;
D) pure void func();

<details>
<summary>✅ Check Answer</summary>

Answer: C) virtual void func() = 0;

💡 Syntax: virtual ReturnType functionName() = 0;

</details>

---

Q9. An interface in C++ is implemented using:

A) A class with all concrete methods
B) A class with all pure virtual functions
C) A struct with public data only
D) A global function

<details>
<summary>✅ Check Answer</summary>

Answer: B) A class with all pure virtual functions

💡 Interface = pure abstract class (all methods are pure virtual).

</details>

---

Q10. Which of the following is NOT a characteristic of an interface?

A) Cannot be instantiated
B) Contains only abstract methods
C) Can have data members
D) All methods are public

<details>
<summary>✅ Check Answer</summary>

Answer: C) Can have data members

💡 Interfaces typically have no data members (no state).

</details>

---

Q11. What is the main difference between an abstract class and an interface?

A) No difference — they are the same
B) Abstract class can have concrete methods; interface has only abstract methods
C) Interface can have data members; abstract class cannot
D) Abstract class cannot be inherited

<details>
<summary>✅ Check Answer</summary>

Answer: B) Abstract class can have concrete methods; interface has only abstract methods

💡 Abstract class = partial implementation. Interface = pure contract.

</details>

---

Q12. A class that implements an interface must:

A) Only inherit it
B) Provide implementation for all pure virtual functions
C) Ignore the abstract methods
D) Create objects of the interface

<details>
<summary>✅ Check Answer</summary>

Answer: B) Provide implementation for all pure virtual functions

💡 Derived class must override all pure virtual functions.

</details>

---

Q13. Which of the following best describes a pure virtual function?

A) A function with no name
B) A function with no return type
C) A function declared with = 0 and no implementation in base class
D) A function that returns void

<details>
<summary>✅ Check Answer</summary>

Answer: C) A function declared with = 0 and no implementation in base class

💡 Pure virtual = abstract method; must be overridden in derived class.

</details>

---

Q14. Abstraction helps in reducing:

A) Code execution speed
B) Complexity for the user
C) Number of classes
D) Memory usage only

<details>
<summary>✅ Check Answer</summary>

Answer: B) Complexity for the user

💡 Users focus on essential features; internal complexity is hidden.

</details>

---

Q15. Which of the following is a real-world example of abstraction?

A) Reading a book's content
B) Using an ATM machine (withdraw, deposit) without knowing internal banking
C) Writing code in a text editor
D) Saving a file with its full path

<details>
<summary>✅ Check Answer</summary>

Answer: B) Using an ATM machine (withdraw, deposit) without knowing internal banking

💡 ATM = simple interface; complex banking system is hidden.

</details>

---

Q16. Abstraction exists at which two levels?

A) Public and private
B) Design level and implementation level
C) Static and dynamic
D) Shallow and deep

<details>
<summary>✅ Check Answer</summary>

Answer: B) Design level and implementation level

💡 Design = architecture/UML. Implementation = abstract classes/interfaces.

</details>

---

Q17. Which level of abstraction focuses on essential features and relationships in design?

A) Implementation level
B) Code level
C) Design level
D) Execution level

<details>
<summary>✅ Check Answer</summary>

Answer: C) Design level

💡 Design level = UML diagrams, architecture design.

</details>

---

Q18. If a derived class does NOT override all pure virtual functions of the base class, then:

A) The program runs normally
B) The derived class also becomes abstract
C) A compile-time error occurs
D) The base class becomes concrete

<details>
<summary>✅ Check Answer</summary>

Answer: B) The derived class also becomes abstract

💡 Unimplemented pure virtual functions make the derived class abstract too.

</details>

---

Q19. Which of the following is an advantage of abstraction?

A) Exposes all implementation details
B) Makes code more complex
C) Improves code reusability
D) Removes the need for classes

<details>
<summary>✅ Check Answer</summary>

Answer: C) Improves code reusability

💡 Abstract classes/interfaces can be reused across the application.

</details>

---

Q20. The main difference between encapsulation and abstraction is:

A) There is no difference
B) Encapsulation hides data; abstraction hides complexity
C) Abstraction hides data; encapsulation hides complexity
D) Both hide the same things

<details>
<summary>✅ Check Answer</summary>

Answer: B) Encapsulation hides data; abstraction hides complexity

💡 Encapsulation = data security. Abstraction = showing essentials, hiding details.

</details>

---

Q21. Which of the following is true about abstraction?

A) It shows all details of implementation
B) It allows direct access to private data
C) It hides implementation details and shows only essential features
D) It makes all methods private

<details>
<summary>✅ Check Answer</summary>

Answer: C) It hides implementation details and shows only essential features

💡 Core definition of abstraction.

</details>

---

Q22. A class with at least one pure virtual function is called:

A) Concrete class
B) Abstract class
C) Interface
D) Final class

<details>
<summary>✅ Check Answer</summary>

Answer: B) Abstract class

💡 At least one = 0 function → abstract class.

</details>

---

Q23. Multiple inheritance using interfaces is:

A) Not allowed in C++
B) Allowed — a class can implement multiple interfaces
C) Causes automatic error
D) Only allowed for abstract classes

<details>
<summary>✅ Check Answer</summary>

Answer: B) Allowed — a class can implement multiple interfaces

💡 Interface (pure abstract class) supports multiple inheritance in C++.

</details>

---

Q24. Which benefit of abstraction allows implementation to change without affecting users?

A) Simplifies model
B) Reduces complexity
C) Provides flexibility
D) Enhances security

<details>
<summary>✅ Check Answer</summary>

Answer: C) Provides flexibility

💡 As long as interface remains same, internal changes don't affect users.

</details>

---

Q25. In the car example, which of the following is a hidden implementation detail?

A) Steering wheel
B) Brake pedal
C) Engine working mechanism
D) Accelerator pedal

<details>
<summary>✅ Check Answer</summary>

Answer: C) Engine working mechanism

💡 Steering wheel, pedals = essential features (shown). Engine = hidden.

</details>

---

Q26. What makes a class an abstract class in C++?

A) Having a virtual destructor
B) Having at least one pure virtual function
C) Having all private members
D) Using the abstract keyword

<details>
<summary>✅ Check Answer</summary>

Answer: B) Having at least one pure virtual function

💡 C++ has no abstract keyword. Pure virtual function makes class abstract.

</details>

---

Q27. The keyword override in C++ is used to:

A) Create a new function
B) Explicitly indicate that a function overrides a base class virtual function
C) Make a function pure virtual
D) Delete a function

<details>
<summary>✅ Check Answer</summary>

Answer: B) Explicitly indicate that a function overrides a base class virtual function

💡 override ensures the function is correctly overriding a virtual function.

</details>

---

Q28. Which scenario is most suitable for using an interface over an abstract class?

A) When you need shared code among related classes
B) When you need to store state (data members)
C) When unrelated classes need to share a common behavior
D) When you need a base class with partial implementation

<details>
<summary>✅ Check Answer</summary>

Answer: C) When unrelated classes need to share a common behavior

💡 Interface = defines contract for any class, related or unrelated.

</details>

---

Q29. Abstraction enhances security by:

A) Making all data public
B) Hiding implementation details from users
C) Allowing direct memory access
D) Removing all methods

<details>
<summary>✅ Check Answer</summary>

Answer: B) Hiding implementation details from users

💡 Hidden details prevent misuse or accidental modification.

</details>

---

Q30. In the Person example (Student, Teacher, Employee), each view shows:

A) All attributes of Person
B) Only attributes relevant to that perspective
C) No attributes at all
D) Random attributes

<details>
<summary>✅ Check Answer</summary>

Answer: B) Only attributes relevant to that perspective

💡 Student shows rollNo, grades. Teacher shows subjects, salary. Different abstractions.

</details>

---

Q31. Which of the following is NOT an advantage of abstraction?

A) Simplifies model
B) Reduces complexity
C) Exposes all internal details
D) Improves maintainability

<details>
<summary>✅ Check Answer</summary>

Answer: C) Exposes all internal details

💡 Abstraction hides details; it does not expose them.

</details>

---

Q32. In C++, a virtual destructor in an abstract base class is important because:

A) It makes the class abstract
B) It ensures proper cleanup of derived class objects through base class pointer
C) It has no use
D) It prevents inheritance

<details>
<summary>✅ Check Answer</summary>

Answer: B) It ensures proper cleanup of derived class objects through base class pointer

💡 Virtual destructor = proper polymorphic deletion.

</details>

---

Q33. Which of the following best describes loose coupling?

A) Classes are heavily dependent on each other
B) Classes depend on interfaces, not concrete implementations
C) All code is in one class
D) No methods are used

<details>
<summary>✅ Check Answer</summary>

Answer: B) Classes depend on interfaces, not concrete implementations

💡 Interfaces promote loose coupling—implementation can be swapped easily.

</details>

---

Q34. A coffee machine's button (press → get coffee) is a good example of:

A) Encapsulation
B) Polymorphism
C) Abstraction
D) Inheritance

<details>
<summary>✅ Check Answer</summary>

Answer: C) Abstraction

💡 Simple interface (button); complex internals (heating, grinding) are hidden.

</details>

---

Q35. When a same object is viewed differently from different perspectives, this demonstrates:

A) Encapsulation
B) Inheritance
C) Polymorphism
D) Abstraction

<details>
<summary>✅ Check Answer</summary>

Answer: D) Abstraction

💡 Different perspectives = different abstractions of the same entity.

</details>

---
