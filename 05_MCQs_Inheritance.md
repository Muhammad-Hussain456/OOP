### ✅ **C++ Inheritance — MCQs

1. **Which access specifiers can be used for inheritance in C++?**
   a) public b) private c) protected d) All of the above
   **✔ Answer:** d) All of the above

   > C++ supports three inheritance visibility modes: public, private, and protected. 

2. **What type of inheritance leads to the *diamond problem*?**
   a) Single b) Multilevel c) Multiple d) Hierarchical
   **✔ Answer:** c) Multiple

   > The diamond problem occurs when multiple inheritance creates ambiguity due to a shared base class.

3. **If no access specifier is given, inherited members are by default:**
   a) public b) private c) protected d) None
   **✔ Answer:** b) private

   > Default inheritance for a `class` is private. 

4. **In C++, which members of the base class are inherited?**
   a) All b) Private only c) Public and protected d) None
   **✔ Answer:** c) Public and protected

   > Private members are not inherited (only accessible inside the base class).
   
5. **Which of the following cannot be inherited?**
   a) Constructor b) Destructor c) Friend functions d) All
   **✔ Answer:** d) All

   > Constructors, destructors, and friend functions are not inherited. 

6. **A class derived from more than one base class uses:**
   a) Single Inheritance b) Multiple c) Hierarchical d) Multilevel
   **✔ Answer:** b) Multiple

   > More than one base means multiple inheritance. 

7. **Multiple derived classes from one base illustrate:**
   a) Single b) Hierarchical c) Multilevel d) Hybrid
   **✔ Answer:** b) Hierarchical

   > One base, many derived = hierarchical. 

8. **What relationship does inheritance represent?**
   a) has‑a b) uses‑a c) is‑a d) part‑of
   **✔ Answer:** c) is‑a

   > Inheritance models “is‑a” relationships. 

9. **Private inheritance means base class members become:**
   a) public b) protected c) private d) inaccessible
   **✔ Answer:** c) private

   > Public and protected base members become private. 

10. **Which type of inheritance involves a chain of levels?**
    a) Multiple b) Multilevel c) Hierarchical d) Hybrid
    **✔ Answer:** b) Multilevel

    > One class derives from another in a chain. 

11. **How many types of inheritance are typically described in C++?**
    a) 2 b) 3 c) 4 d) 5
    **✔ Answer:** d) 5

    > C++ inheritance is commonly categorized into five types: single, multilevel, multiple, hierarchical, and hybrid. 

12. **Can constructors of the base class be inherited?**
    a) Yes b) No c) Only constructors d) Depends on compiler
    **✔ Answer:** b) No

    > Constructors (and destructors) are not inherited. 

13. **When a derived object is destroyed, which destructor runs first?**
    a) Base b) Derived c) Both simultaneously d) Random
    **✔ Answer:** b) Derived

    > Derived destructor runs before base destructor. 

14. **In public inheritance, base class public members become:**
    a) public b) private c) protected d) inaccessible
    **✔ Answer:** a) public

    > Public inheritance preserves base member visibility. 

15. **In private inheritance, protected members of base become:**
    a) public b) private c) protected d) inaccessible
    **✔ Answer:** b) private

    > Protected becomes private. 

16. **A derived class can access protected base class members:**
    a) Yes b) No c) Only in public inheritance d) Only in multiple inheritance
    **✔ Answer:** a) Yes

    > Protected members are accessible to derived classes. 

17. **What is function overriding?**
    a) Changing operator behavior b) Redefining base class function in derived class c) Having multiple functions with same name in base d) None
    **✔ Answer:** b) Redefining base class function in derived class

    > Redefinition in derived class is overriding. 

18. **Making a base class function `virtual` enables:**
    a) Early binding b) Dynamic binding c) Bigger objects d) Preventing inheritance
    **✔ Answer:** b) Dynamic binding

    > `virtual` enables runtime polymorphism. 

19. **In hybrid inheritance, the structure involves:**
    a) Single + multiple b) Multiple + multilevel c) Hierarchical + multilevel d) Any combination
    **✔ Answer:** d) Any combination

    > Hybrid is a combination of inheritance types. 

20. **The syntax to declare inheritance is:**
    a) `class D inherits B` b) `class D : access B` c) `class D : access specifier B` d) `class D extends B`
    **✔ Answer:** c) `class D : access specifier B`

    > C++ uses colon + specifier before base name. 

---

