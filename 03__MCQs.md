
## Practice MCQs:  Properties and Methods (C++)

---

Q1. What are the two main components of a class in OOP?

A) Variables and Constants
B) Properties and Methods
C) Objects and Functions
D) Pointers and References

<details>
<summary>✅ Check Answer</summary>

Answer: B) Properties and Methods

💡 Properties store state/data; Methods define actions/behaviors.

</details>

---

Q2. Properties of a class are also known as:

A) Member Functions
B) Behaviors
C) Data Members
D) Constructors

<details>
<summary>✅ Check Answer</summary>

Answer: C) Data Members

💡 Properties = Attributes = Data Members = Fields (store state).

</details>

---

Q3. Methods of a class are also known as:

A) Attributes
B) Data Members
C) Fields
D) Member Functions

<details>
<summary>✅ Check Answer</summary>

Answer: D) Member Functions

💡 Methods = Member Functions = Behaviors (define actions).

</details>

---

Q4. What is the purpose of properties in a class?

A) Define actions/behaviors
B) Store the state/data of an object
C) Destroy objects
D) Overload operators

<details>
<summary>✅ Check Answer</summary>

Answer: B) Store the state/data of an object

💡 Properties hold data like name, rollNo, GPA.

</details>

---

Q5. A function defined inside the class body is by default:

A) A static function
B) A virtual function
C) An inline function
D) A friend function

<details>
<summary>✅ Check Answer</summary>

Answer: C) An inline function

💡 Inside class = implicitly inline. Reduces function call overhead.

</details>

---

Q6. Which operator is used to define a member function outside the class?

A) Dot operator (.)
B) Arrow operator (->)
C) Scope resolution operator (::)
D) Assignment operator (=)

<details>
<summary>✅ Check Answer</summary>

Answer: C) Scope resolution operator (::)

💡 Syntax: ReturnType ClassName::functionName() { }

</details>

---

Q7. What is the primary benefit of inline functions?

A) Increase code size
B) Reduce function call overhead
C) Enable polymorphism
D) Allow inheritance

<details>
<summary>✅ Check Answer</summary>

Answer: B) Reduce function call overhead

💡 Code is inserted at call point instead of a normal function call.

</details>

---

Q8. The keyword inline is a _______ to the compiler.

A) Command
B) Directive
C) Request
D) Obligation

<details>
<summary>✅ Check Answer</summary>

Answer: C) Request

💡 Compiler may ignore it—it's not a command.

</details>

---

Q9. What happens if the compiler ignores the inline keyword?

A) Compilation error occurs
B) The function is treated as a normal function
C) The program crashes
D) The function becomes static

<details>
<summary>✅ Check Answer</summary>

Answer: B) The function is treated as a normal function

💡 No error—just standard function call overhead applies.

</details>

---

Q10. Which of the following is true about constructors?

A) They have a return type
B) They must be called explicitly
C) Their name is the same as the class name
D) They can be called multiple times per object

<details>
<summary>✅ Check Answer</summary>

Answer: C) Their name is the same as the class name

💡 Constructor name matches class name, no return type, called once automatically.

</details>

---

Q11. What is the return type of a constructor?

A) void
B) int
C) No return type (not even void)
D) bool

<details>
<summary>✅ Check Answer</summary>

Answer: C) No return type (not even void)

💡 Constructors have no return type at all.

</details>

---

Q12. When is a constructor called?

A) Manually by the programmer
B) Automatically at object creation
C) When the program ends
D) Only when explicitly invoked

<details>
<summary>✅ Check Answer</summary>

Answer: B) Automatically at object creation

💡 Constructors initialize objects automatically at creation.

</details>

---

Q13. How many times can a constructor be called for a single object?

A) Zero times
B) Once
C) Twice
D) Unlimited times

<details>
<summary>✅ Check Answer</summary>

Answer: B) Once

💡 Once per object, at creation time only.

</details>

---

Q14. A constructor that takes no parameters is called a:

A) Copy constructor
B) Parameterized constructor
C) Default constructor
D) Inline constructor

<details>
<summary>✅ Check Answer</summary>

Answer: C) Default constructor

💡 No parameters. Compiler generates one if none defined.

</details>

---

Q15. What is the default value of an int data member when initialized by the compiler-generated default constructor?

A) -1
B) 1
C) Garbage value
D) 0

<details>
<summary>✅ Check Answer</summary>

Answer: D) 0

💡 int/float → 0/0.0; pointer → nullptr/NULL.

</details>

---

Q16. What is the default value of a pointer data member when initialized by the compiler-generated default constructor?

A) 0
B) nullptr / NULL
C) Pointing to a random memory location
D) 1

<details>
<summary>✅ Check Answer</summary>

Answer: B) nullptr / NULL

💡 Pointers default to nullptr/NULL, not random memory.

</details>

---

Q17. Having multiple constructors with different parameter lists is called:

A) Function overriding
B) Function overloading
C) Constructor overloading
D) Operator overloading

<details>
<summary>✅ Check Answer</summary>

Answer: C) Constructor overloading

💡 Multiple constructors with different parameters.

</details>

---

Q18. Which feature allows using default values in constructor parameters to reduce the number of constructors / to avoid  use of multiple constructors?

A) Copy constructor
B) Inline functions
C) Default parameters
D) Destructors

<details>
<summary>✅ Check Answer</summary>

Answer: C) Default parameters

💡 Example: Student(char *aName = NULL, int aRollNo = 0, float aGPA = 0.0);

</details>

---

Q19. A copy constructor is called when:

A) An object is deleted
B) An object is initialized from another object
C) A member function is called
D) The program starts

<details>
<summary>✅ Check Answer</summary>

Answer: B) An object is initialized from another object

💡 Also called when passing/returning objects by value.

</details>

---

Q20. In a shallow copy, what happens to pointer members?

A) New memory is allocated
B) Only the address is copied
C) The pointer is set to NULL
D) The data is deep-copied

<details>
<summary>✅ Check Answer</summary>

Answer: B) Only the address is copied

💡 Default compiler behavior. Both objects point to same memory.

</details>

---

Q21. What is the main problem with shallow copy when pointers are involved?

A) Memory leak only
B) Shared memory issue (both objects point to the same memory)
C) Compilation error
D) Objects cannot be created

<details>
<summary>✅ Check Answer</summary>

Answer: B) Shared memory issue (both objects point to the same memory)

💡 Changes via one object affect the other unintentionally.

</details>

---

Q22. A deep copy constructor:

A) Copies only the pointer address
B) Allocates new memory and copies the actual data
C) Deletes the original object
D) Is provided by default by the compiler

<details>
<summary>✅ Check Answer</summary>

Answer: B) Allocates new memory and copies the actual data

💡 Prevents shared memory problems by duplicating pointed data.

</details>

---

Q23. Which of the following is a difference between a constructor and a method?

A) Both have a return type
B) Constructors are inherited, methods are not
C) Constructors have no return type, methods must have a return type
D) Methods are called automatically, constructors are called explicitly

<details>
<summary>✅ Check Answer</summary>

Answer: C) Constructors have no return type, methods must have a return type

💡 Constructors: no return type, called once, not inherited. Methods: have return type, called multiple times, inherited.

</details>

---

Q24. Are constructors inherited in C++?

A) Yes
B) No
C) Only in multiple inheritance
D) Only if declared virtual

<details>
<summary>✅ Check Answer</summary>

Answer: B) No

💡 Constructors are not inherited. Methods are.

</details>

---

Q25. Can constructors be overloaded?

A) Yes
B) No
C) Only default constructor can be overloaded
D) Only copy constructor can be overloaded

<details>
<summary>✅ Check Answer</summary>

Answer: A) Yes

💡 Constructors support overloading like regular methods.

</details>

---

Q26. What is the access specifier typically used for constructors?

A) private
B) protected
C) public
D) static

<details>
<summary>✅ Check Answer</summary>

Answer: C) public

💡 Usually public so objects can be created from outside the class.

</details>

---

Q27. Which of the following is NOT a situation where the copy constructor is called?

A) Object initialization from another object
B) Passing an object by value to a function
C) Returning an object by value from a function
D) Calling a member function on an object

<details>
<summary>✅ Check Answer</summary>

Answer: D) Calling a member function on an object

💡 Member function calls don't invoke copy constructor.

</details>

---

Q28. To make a function defined outside the class inline, you must use the keyword:

A) static
B) extern
C) inline
D) virtual

<details>
<summary>✅ Check Answer</summary>

Answer: C) inline

💡 To make a function defined outside the class as an inline function, we need explicit `inline` keyword.

</details>

---

Q29. Public methods of a class act as the _______ of the class.

A) Data storage
B) Interface
C) Destructor
D) Private member

<details>
<summary>✅ Check Answer</summary>

Answer: B) Interface

💡 Public methods provide the interface for interacting with properties / other methods / objects.

</details>

---

Q30. Which statement correctly declares a default constructor for a class named Student?

A) void Student();
B) Student();
C) int Student();
D) default Student();

<details>
<summary>✅ Check Answer</summary>

Answer: B) Student();

💡 No return type; name matches class name.

</details>

---
