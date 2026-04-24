## Practice MCQs: Encapsulation 

---

Q1. Encapsulation is a fundamental concept of OOP that:

A) Only hides data
B) Bundles data and methods together and controls access to them
C) Only creates objects
D) Only inherits properties

<details>
<summary>✅ Check Answer</summary>

Answer: B) Bundles data and methods together and controls access to them

💡 Encapsulation = Bundling + Data Hiding + Controlled Access

</details>

---

Q2. Which of the following best defines encapsulation?

A) Wrapping data members and member functions into a single unit
B) Creating multiple instances of a class
C) Defining multiple functions with the same name
D) Hiding implementation details from users

<details>
<summary>✅ Check Answer</summary>

Answer: A) Wrapping data members and member functions into a single unit

💡 Core definition: bundling/wrapping data and functions together.

</details>

---

Q3. Which access modifier provides the highest level of data hiding?

A) public
B) private
C) protected
D) static

<details>
<summary>✅ Check Answer</summary>

Answer: B) private

💡 private members are accessible only within the class — complete hiding.

</details>

---

Q4. Data members of a class should ideally be declared as:

A) public
B) private
C) protected
D) global

<details>
<summary>✅ Check Answer</summary>

Answer: B) private

💡 True encapsulation rule: data members → private, methods → public.

</details>

---

Q5. Which of the following is NOT a benefit of encapsulation?

A) Data security
B) Data integrity
C) Direct data access from outside
D) Maintainability

<details>
<summary>✅ Check Answer</summary>

Answer: C) Direct data access from outside

💡 Encapsulation prevents direct access; it provides controlled access.

</details>

---

Q6. How does encapsulation help in achieving data hiding?

A) By making all members public
B) By using private access specifier and providing public methods
C) By using global variables
D) By removing all methods from the class

<details>
<summary>✅ Check Answer</summary>

Answer: B) By using private access specifier and providing public methods

💡 Private hides data; public getters/setters control access.

</details>

---

Q7. The method used to read the value of a private data member is called:

A) Mutator
B) Accessor
C) Constructor
D) Destructor

<details>
<summary>✅ Check Answer</summary>

Answer: B) Accessor

💡 Accessor/Getter = read. Mutator/Setter = write.

</details>

---

Q8. The method used to modify the value of a private data member is called:

A) Accessor
B) Mutator
C) Getter
D) Constructor

<details>
<summary>✅ Check Answer</summary>

Answer: B) Mutator

💡 Mutator/Setter = modifies/writes data. Accessor/Getter = reads data.

</details>

---

Q9. Which of the following is true about encapsulation?

A) It decreases code reusability
B) It increases coupling between classes
C) It helps in hiding implementation details
D) It makes all data public

<details>
<summary>✅ Check Answer</summary>

Answer: C) It helps in hiding implementation details

💡 Internal details stay hidden; only interface is exposed.

</details>

---

Q10. In encapsulation, the internal implementation of a class is:

A) Visible to all users
B) Hidden from outside world
C) Stored outside the class
D) Accessible directly

<details>
<summary>✅ Check Answer</summary>

Answer: B) Hidden from outside world

💡 Implementation details are private, hidden behind public interface.

</details>

---

Q11. What is the main difference between basic encapsulation and true encapsulation?

A) Basic has classes, true does not
B) Basic only bundles; true adds data hiding and controlled access
C) Basic uses private; true uses public
D) There is no difference

<details>
<summary>✅ Check Answer</summary>

Answer: B) Basic only bundles; true adds data hiding and controlled access

💡 Basic = Class/object bundling. True = Private + Getters/Setters + Validation.

</details>

---

Q12. An object in OOP is an example of:

A) Polymorphism
B) Basic encapsulation
C) Inheritance
D) Abstraction only

<details>
<summary>✅ Check Answer</summary>

Answer: B) Basic encapsulation

💡 Object bundles/contains both data and behavior as one unit.

</details>

---

Q13. Which keyword is used to restrict access to class members in C++?

A) restrict
B) limit
C) private
D) hidden

<details>
<summary>✅ Check Answer</summary>

Answer: C) private

💡 private keyword restricts access to within the class only.

</details>

---

Q14. Getters and setters are used to:

A) Directly access private members
B) Provide controlled access to private members
C) Delete data members
D) Create new data members

<details>
<summary>✅ Check Answer</summary>

Answer: B) Provide controlled access to private members

💡 Getters/Setters = controlled read/write interface to hidden data.

</details>

---

Q15. Validation logic inside setters is used to:

A) Increase program size
B) Ensure only valid data is stored in objects
C) Make code slower
D) Bypass encapsulation

<details>
<summary>✅ Check Answer</summary>

Answer: B) Ensure only valid data is stored in objects

💡 Validation prevents invalid data, maintains data integrity.

</details>

---

Q16. Which of the following correctly implements encapsulation?

```cpp
A)  class Test {              B)  class Test {
    public:                       private:
    int x;                        int x;
    };                            public:
                                  void setX(int val) { x = val; }
                                  };

C)  class Test {              D)  None of these
    int x;
    };
```

<details>
<summary>✅ Check Answer</summary>

Answer: B)

💡 Private data + public setter = proper encapsulation.

</details>

---

Q17. What is the significance of the protected access specifier in encapsulation?

A) It allows access only within the class
B) It allows access within the class and derived classes
C) It allows access from anywhere
D) It has no significance

<details>
<summary>✅ Check Answer</summary>

Answer: B) It allows access within the class and derived classes

💡 protected = class itself + child/inherited classes.

</details>

---

Q18. Encapsulation is also known as:

A) Data binding
B) Data hiding
C) Data abstraction
D) Both B and C

<details>
<summary>✅ Check Answer</summary>

Answer: D) Both B and C

💡 Encapsulation = Data Hiding (implementation) + provides abstraction.

</details>

---

Q19. Which of the following statements is FALSE about encapsulation?

A) It provides data security
B) It allows direct modification of private members
C) It bundles data and methods together
D) It improves maintainability

<details>
<summary>✅ Check Answer</summary>

Answer: B) It allows direct modification of private members

💡 Private members CANNOT be accessed directly from outside.

</details>

---

Q20. In true encapsulation, the interface of a class is provided through:

A) Private data members
B) Public member functions
C) Global variables
D) Friend functions only

<details>
<summary>✅ Check Answer</summary>

Answer: B) Public member functions

💡 Public methods = interface. Objects interact only through public methods.

</details>

---

Q21. A class bundles _______ and _______ together.

A) Objects, functions
B) Data members, member functions
C) Variables, loops
D) Headers, source files

<details>
<summary>✅ Check Answer</summary>

Answer: B) Data members, member functions

💡 Class = blueprint that bundles data and methods into one unit.

</details>

---

Q22. Without using access modifiers, a class provides:

A) True encapsulation
B) Basic encapsulation only
C) Complete data hiding
D) No encapsulation at all

<details>
<summary>✅ Check Answer</summary>

Answer: B) Basic encapsulation only

💡 Even without modifiers, class bundles data+methods = basic encapsulation.

</details>

---

Q23. Which of the following represents controlled write access in encapsulation?

A) Constructor
B) Destructor
C) Setter method with validation
D) Direct assignment operator

<details>
<summary>✅ Check Answer</summary>

Answer: C) Setter method with validation

💡 Setters = controlled write. Validation ensures data correctness.

</details>

---

Q24. The main purpose of encapsulation is to:

A) Make all data globally accessible
B) Protect data from unauthorized access and modification
C) Reduce program execution speed
D) Increase code complexity

<details>
<summary>✅ Check Answer</summary>

Answer: B) Protect data from unauthorized access and modification

💡 Protection + controlled access = core purpose of encapsulation.

</details>

---

Q25. In the statement s1.rollNo = -5;, if rollNo is private, this will cause:

A) No error
B) Compile-time error
C) Run-time error
D) Logical error

<details>
<summary>✅ Check Answer</summary>

Answer: B) Compile-time error

💡 Accessing private members from outside the class = compilation error.

</details>

---

Q26. Which of these is a real-world analogy of true encapsulation?

A) A public library with open shelves
B) An ATM machine with PIN protection
C) A park with no fence
D) A transparent glass wall

<details>
<summary>✅ Check Answer</summary>

Answer: B) An ATM machine with PIN protection

💡 ATM: hidden internal mechanism + controlled access via PIN/card.

</details>

---

Q27. How does encapsulation improve code maintainability?

A) By allowing global access to all data
B) By localizing changes to specific methods
C) By removing all functions
D) By using only global variables

<details>
<summary>✅ Check Answer</summary>

Answer: B) By localizing changes to specific methods

💡 Changes to validation/implementation affect only the setter/getter.

</details>

---

Q28. If a class has private data members and no getters/setters, the data is:

A) Fully accessible
B) Completely hidden and inaccessible from outside
C) Partially accessible
D) Automatically public

<details>
<summary>✅ Check Answer</summary>

Answer: B) Completely hidden and inaccessible from outside

💡 Without getters/setters, private data is unreachable from outside.

</details>

---

Q29. The keyword private in a class ensures:

A) All members are accessible globally
B) Members are accessible only within the class
C) Members are accessible in derived classes only
D) Members are deleted after use

<details>
<summary>✅ Check Answer</summary>

Answer: B) Members are accessible only within the class

💡 private = access limited to the class where declared.

</details>

---

Q30. Encapsulation and data hiding are:

A) Exactly the same concepts
B) Completely unrelated
C) Related; encapsulation facilitates data hiding
D) Opposite concepts

<details>
<summary>✅ Check Answer</summary>

Answer: C) Related; encapsulation facilitates data hiding

💡 Encapsulation is the mechanism that enables data hiding.

</details>

---

Q31. Which programming construct(s) are used for true encapsulation?

A) Only classes
B) Access modifiers, getters, setters, and validation
C) Only objects
D) Only constructors

<details>
<summary>✅ Check Answer</summary>

Answer: B) Access modifiers, getters, setters, and validation

💡 True encapsulation = private + public getters/setters + validation.

</details>

---

Q32. The ability of an object to prevent invalid data from being stored is called:

A) Polymorphism
B) Data integrity
C) Inheritance
D) Abstraction

<details>
<summary>✅ Check Answer</summary>

Answer: B) Data integrity

💡 Validation in setters ensures data integrity (data stays valid).

</details>

---

Q33. Which of these provides read-only access to private members?

A) Constructor
B) Setter method
C) Getter method
D) Friend function

<details>
<summary>✅ Check Answer</summary>

Answer: C) Getter method

💡 Getter/Accessor = read-only controlled access.

</details>

---

Q34. In C++, the default access specifier for class members is:

A) public
B) private
C) protected
D) global

<details>
<summary>✅ Check Answer</summary>

Answer: B) private

💡 In C++, class members are private by default (unlike struct).

</details>

---

Q35. A well-encapsulated class should have:

A) All members public
B) Data members private, essential methods public
C) All members private
D) No methods at all

<details>
<summary>✅ Check Answer</summary>

Answer: B) Data members private, essential methods public

💡 Rule: Hide data (private), expose interface (public methods).

</details>

---
