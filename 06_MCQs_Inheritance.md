## Practice MCQs: Inheritance

---

Q1. Inheritance is a mechanism where a derived class:

A) Deletes properties of the base class
B) Inherits properties and behaviors from a base class
C) Cannot access base class members
D) Creates objects of the base class

<details>
<summary>✅ Check Answer</summary>

Answer: B) Inherits properties and behaviors from a base class

💡 Inheritance = child class gets parent's characteristics. Major benefit is reuse.

</details>

---

Q2. The major benefit of inheritance is:

A) Data hiding
B) Code reuse
C) Complexity increase
D) Memory allocation

<details>
<summary>✅ Check Answer</summary>

Answer: B) Code reuse

💡 Main purpose of inheritance is reuse. Add new classes by inheriting existing ones.

</details>

---

Q3. In inheritance, the parent class is called:

A) Derived class
B) Child class
C) Base class
D) Subclass

<details>
<summary>✅ Check Answer</summary>

Answer: C) Base class

💡 Parent class = Base class. Child class = Derived class.

</details>

---

Q4. Besides inherited characteristics, a derived class may have:

A) No additional features
B) Its own unique characteristics
C) Only base class features
D) Less features than base class

<details>
<summary>✅ Check Answer</summary>

Answer: B) Its own unique characteristics

💡 Derived class inherits all base characteristics plus can add its own.

</details>

---

Q5. Inheritance represents which type of relationship?

A) HAS-A
B) USES-A
C) IS-A or IS-A-KIND-OF
D) CREATES-A

<details>
<summary>✅ Check Answer</summary>

Answer: C) IS-A or IS-A-KIND-OF

💡 Each derived class is a special kind of its base class. Example: Teacher IS-A Person.

</details>

---

Q6. In the Person-Teacher-Student hierarchy, which is the base class?

A) Teacher
B) Student
C) Doctor
D) Person

<details>
<summary>✅ Check Answer</summary>

Answer: D) Person

💡 Person is the parent/base class. Teacher, Student, Doctor are derived classes.

</details>

---

Q7. Generalization is the process of:

A) Adding specific features to a class
B) Extracting common characteristics from multiple classes into a base class
C) Deleting redundant classes
D) Creating objects from classes

<details>
<summary>✅ Check Answer</summary>

Answer: B) Extracting common characteristics from multiple classes into a base class

💡 Generalization = extract shared features → create new base class.

</details>

---

Q8. Generalization is a _______ process.

A) Top-down
B) Horizontal
C) Bottom-up
D) Random

<details>
<summary>✅ Check Answer</summary>

Answer: C) Bottom-up

💡 Generalization: Specific classes → General base class (bottom-up direction).

</details>

---

Q9. Which of the following is a purpose of generalization?

A) Increase redundancy
B) Reduce redundancy and promote reuse
C) Make code more complex
D) Prevent inheritance

<details>
<summary>✅ Check Answer</summary>

Answer: B) Reduce redundancy and promote reuse

💡 Generalization reduces redundancy, improves maintainability, promotes reuse.

</details>

---

Q10. Before generalization, Circle, Line, and Triangle each had duplicate attributes like color and vertices. This represents:

A) Good design
B) Code redundancy
C) Polymorphism
D) Abstraction

<details>
<summary>✅ Check Answer</summary>

Answer: B) Code redundancy

💡 Common features duplicated across classes → generalization solves this.

</details>

---

Q11. Sub-typing (Extension) occurs when a derived class:

A) Restricts the base class behavior
B) Extends characteristics without violating base class expectations
C) Hides all base class features
D) Cannot be instantiated

<details>
<summary>✅ Check Answer</summary>

Answer: B) Extends characteristics without violating base class expectations

💡 Sub-typing = adds new features while preserving behavioral compatibility.

</details>

---

Q12. Behavioral compatibility in sub-typing means:

A) Base class can never be used
B) Base class can be replaced by derived class
C) Derived class cannot be used
D) Both classes are identical

<details>
<summary>✅ Check Answer</summary>

Answer: B) Base class can be replaced by derived class

💡 Liskov Substitution Principle: derived class is behaviorally compatible.

</details>

---

Q13. If Student inherits from Person and adds study() and takeExam(), this is an example of:

A) Specialization (Restriction)
B) Generalization
C) Sub-typing (Extension)
D) Abstraction

<details>
<summary>✅ Check Answer</summary>

Answer: C) Sub-typing (Extension)

💡 Student extends Person with new methods (study, takeExam) + preserves base behavior.

</details>

---

Q14. Specialization (Restriction) occurs when a derived class:

A) Only adds new methods
B) Adds constraints or validation to base class behavior
C) Has no relationship with base class
D) Cannot override methods

<details>
<summary>✅ Check Answer</summary>

Answer: B) Adds constraints or validation to base class behavior

💡 Specialization = restricts base class by adding constraints.

</details>

---

Q15. In Specialization, the derived class may be:

A) Always larger than base class
B) Behaviorally incompatible with base class in some aspects
C) Identical to base class
D) Always abstract

<details>
<summary>✅ Check Answer</summary>

Answer: B) Behaviorally incompatible with base class in some aspects

💡 Base class cannot always be replaced by derived class due to restrictions.

</details>

---

Q16. If IntegerSet allows add(-5) but NaturalSet rejects add(-5), this is an example of:

A) Sub-typing (Extension)
B) Generalization
C) Specialization (Restriction)
D) Abstraction

<details>
<summary>✅ Check Answer</summary>

Answer: C) Specialization (Restriction)

💡 NaturalSet restricts IntegerSet: adds constraint that only positive numbers allowed.

</details>

---

Q17. In the Adult class (derived from Person), age is restricted to 18-100. setAge(15) is rejected. This is:

A) Sub-typing
B) Specialization (Restriction)
C) Generalization
D) Polymorphism

<details>
<summary>✅ Check Answer</summary>

Answer: B) Specialization (Restriction)

💡 Adult restricts Person's age range. Invalid ages are rejected.

</details>

---

Q18. Method overriding means:

A) Creating a new method with different name
B) Modifying/redefining the default behavior provided by parent class
C) Deleting the parent method
D) Copying the parent method exactly

<details>
<summary>✅ Check Answer</summary>

Answer: B) Modifying/redefining the default behavior provided by parent class

💡 Overriding = child class modifies inherited method behavior.

</details>

---

Q19. When each shape (Circle, Line, Triangle) overrides draw() to provide its own specific drawing behavior, this is overriding for:

A) Extension
B) Restriction
C) Specific behavior
D) Performance

<details>
<summary>✅ Check Answer</summary>

Answer: C) Specific behavior

💡 Each child implements the same method differently for its unique needs.

</details>

---

Q20. When DialogBox.open() calls super.open() first and then adds extra functionality, this is overriding for:

A) Specific behavior
B) Extension
C) Restriction
D) Performance improvement

<details>
<summary>✅ Check Answer</summary>

Answer: B) Extension

💡 Extends parent behavior by adding extra steps while preserving original.

</details>

---

Q21. When NaturalSet.add() throws an exception for negative numbers, this is overriding for:

A) Extension
B) Specific behavior
C) Restriction
D) Performance

<details>
<summary>✅ Check Answer</summary>

Answer: C) Restriction

💡 Restricts behavior by adding validation that limits what method can do.

</details>

---

Q22. When Circle overrides rotate() with a null operation (does nothing because a rotated circle looks the same), this is overriding for:

A) Specific behavior
B) Extension
C) Restriction
D) Performance improvement

<details>
<summary>✅ Check Answer</summary>

Answer: D) Performance improvement

💡 Circle.rotate() = O(1) null operation; Polygon.rotate() = O(n) complex calculation.

</details>

---

Q23. An abstract class:

A) Can be instantiated directly
B) Cannot be instantiated
C) Contains only concrete methods
D) Has no derived classes

<details>
<summary>✅ Check Answer</summary>

Answer: B) Cannot be instantiated

💡 Abstract class represents incomplete concept — cannot create objects directly.

</details>

---

Q24. Why can't abstract classes be instantiated?

A) They have too many methods
B) They represent incomplete/abstract concepts
C) They have no methods
D) They are too specific

<details>
<summary>✅ Check Answer</summary>

Answer: B) They represent incomplete/abstract concepts

💡 "Vehicle" is too generic — you need a specific Car, Bike, or Truck.

</details>

---

Q25. An abstract class can contain:

A) Only abstract methods
B) Both abstract and concrete methods
C) Only concrete methods
D) No methods at all

<details>
<summary>✅ Check Answer</summary>

Answer: B) Both abstract and concrete methods

💡 Abstract class = abstract methods + concrete methods + data members.

</details>

---

Q26. The main purpose of an abstract class is:

A) To be instantiated directly
B) To be inherited by other classes
C) To hide all data
D) To replace all concrete classes

<details>
<summary>✅ Check Answer</summary>

Answer: B) To be inherited by other classes

💡 Abstract class = blueprint + contract. Designed to be inherited from.

</details>

---

Q27. In the Vehicle hierarchy, accelerate() and applyBrakes() are shared by all vehicles. These are examples of:

A) Abstract methods
B) Concrete methods in abstract class
C) Pure virtual functions
D) Private methods

<details>
<summary>✅ Check Answer</summary>

Answer: B) Concrete methods in abstract class

💡 Abstract class can have fully implemented (concrete) methods shared by children.

</details>

---

Q28. In the Vehicle hierarchy, start(), stop(), and honk() must be implemented differently by each vehicle. These are:

A) Concrete methods
B) Abstract methods
C) Static methods
D) Private methods

<details>
<summary>✅ Check Answer</summary>

Answer: B) Abstract methods

💡 Abstract methods = no implementation in base; must be implemented in derived.

</details>

---

Q29. A concrete class:

A) Cannot be instantiated
B) Represents a real-world object that can be instantiated
C) Contains only abstract methods
D) Has no implementation

<details>
<summary>✅ Check Answer</summary>

Answer: B) Represents a real-world object that can be instantiated

💡 Concrete class = complete implementation + objects can be created.

</details>

---

Q30. In the Person hierarchy, which class can be instantiated?

A) Person (abstract)
B) Student, Teacher, Doctor (concrete)
C) All of them
D) None of them

<details>
<summary>✅ Check Answer</summary>

Answer: B) Student, Teacher, Doctor (concrete)

💡 Person is abstract (cannot instantiate). Concrete subclasses can be instantiated.

</details>

---

Q31. Which of the following is an example of an abstract class?

A) Car
B) Bike
C) Vehicle
D) Truck

<details>
<summary>✅ Check Answer</summary>

Answer: C) Vehicle

💡 Vehicle = abstract concept. Car, Bike, Truck = concrete implementations.

</details>

---

Q32. The relationship between abstract class and concrete class is:

A) Abstract class is the implementation; concrete class is the contract
B) Abstract class provides blueprint/contract; concrete classes complete the implementation
C) Both are completely independent
D) Concrete class inherits nothing from abstract class

<details>
<summary>✅ Check Answer</summary>

Answer: B) Abstract class provides blueprint/contract; concrete classes complete the implementation

💡 Concrete classes complete/fulfill the abstraction.

</details>

---

Q33. Which concept involves extracting common features from Circle, Line, and Triangle into Shape?

A) Specialization
B) Sub-typing
C) Generalization
D) Overriding

<details>
<summary>✅ Check Answer</summary>

Answer: C) Generalization

💡 Generalization = bottom-up extraction of common characteristics into base class.

</details>

---

Q34. Which concept creates specific classes like Student, Teacher from a general Person class?

A) Generalization
B) Specialization
C) Encapsulation
D) Abstraction

<details>
<summary>✅ Check Answer</summary>

Answer: B) Specialization

💡 Specialization = top-down creation of specific derived classes from general base.

</details>

---

Q35. The direction of specialization is:

A) Bottom-up
B) Horizontal
C) Top-down
D) Circular

<details>
<summary>✅ Check Answer</summary>

Answer: C) Top-down

💡 Specialization: General base class → Specific derived classes (top-down).

</details>

---

Q36. Which of the following follows the Liskov Substitution Principle (LSP)?

A) Specialization (Restriction)
B) Sub-typing (Extension)
C) Both equally
D) Neither

<details>
<summary>✅ Check Answer</summary>

Answer: B) Sub-typing (Extension)

💡 Sub-typing = behaviorally compatible. Specialization may violate LSP.

</details>

---

Q37. Multiple inheritance can lead to which challenge?

A) Increased simplicity
B) Duplicate features and ambiguity
C) Better performance
D) Less code

<details>
<summary>✅ Check Answer</summary>

Answer: B) Duplicate features and ambiguity

💡 Multiple inheritance challenges: increased complexity, duplicate features, ambiguity.

</details>

---

Q38. The solution to ambiguity caused by duplicate features in multiple inheritance is:

A) Delete one parent
B) Override the common feature
C) Ignore the problem
D) Make all classes abstract

<details>
<summary>✅ Check Answer</summary>

Answer: B) Override the common feature

💡 Override resolves ambiguity from multiple parents.

</details>

---

Q39. In C++, a pure virtual function is used to create:

A) Concrete classes
B) Abstract methods
C) Static methods
D) Global functions

<details>
<summary>✅ Check Answer</summary>

Answer: B) Abstract methods

💡 Pure virtual function (= 0) = abstract method in C++.

</details>

---

Q40. Which of the following is NOT a benefit of inheritance?

A) Code reusability
B) Hierarchical organization
C) Extensibility
D) Data hiding

<details>
<summary>✅ Check Answer</summary>

Answer: D) Data hiding

💡 Inheritance benefits: reuse, hierarchy, extensibility. Data hiding = encapsulation.

</details>

---

Q41. According to the notes, we can easily add new classes by:

A) Modifying existing classes extensively
B) Inheriting from existing classes and adding/modifying functionality
C) Deleting all existing classes
D) Creating classes without any relationship

<details>
<summary>✅ Check Answer</summary>

Answer: B) Inheriting from existing classes and adding/modifying functionality

💡 Select existing class close to desired functionality → inherit → add/modify.

</details>

---

Q42. Method overriding is used to implement:

A) Encapsulation
B) Abstraction
C) Polymorphism
D) Data hiding

<details>
<summary>✅ Check Answer</summary>

Answer: C) Polymorphism

💡 Method overriding is used to implement polymorphism (discussed in Polymorphism topic).

</details>

---

Q43. An abstract class represents a concept that is:

A) Complete and ready to use
B) Incomplete and too generic to instantiate
C) Always without any methods
D) The most specific in hierarchy

<details>
<summary>✅ Check Answer</summary>

Answer: B) Incomplete and too generic to instantiate

💡 "Shape" is abstract — you need a specific shape like Circle or Rectangle.

</details>

---

Q44. A concrete class represents a concept that is:

A) Abstract and incomplete
B) Complete and ready for instantiation
C) Never instantiated
D) Always the base class

<details>
<summary>✅ Check Answer</summary>

Answer: B) Complete and ready for instantiation

💡 Concrete class = full implementation + can create objects.

</details>

---

Q45. In overriding for extension, the child class method:

A) Completely replaces the parent method
B) Calls the parent method and adds extra functionality
C) Deletes the parent method
D) Ignores the parent method

<details>
<summary>✅ Check Answer</summary>

Answer: B) Calls the parent method and adds extra functionality

💡 DialogBox.open() calls super.open() first, then adds content loading and buttons.

</details>

---
