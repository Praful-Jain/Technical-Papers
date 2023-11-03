# SOLID Principles of Object Oriented and Agile design.

## Object Oriented
- Object oriented is about managing dependencies by selectively re-inverting certain key dependencies in your architecture so that you can prevent rigidity, fragility, non-reusability of code.
- Rigid Code - Code that has dependencies by others, such that you cannot make any isolated change.
- Fragility - Fragility is the tendency of the code to break in many places, even if you only changed at one placw.
- So, in order to reduce the rigitidy and fragility of our code there are certain principles defined called the SOLID principles.

## SOLID Principles
1. The Single Responsibility Principle (SRP) -
   - Don't put functions that change for different reasons in the same class.
   - A class should have one and only one reason to change.

2. Open/Closed Principle -
   - Modules should be open for extension but closed for modification.
   - Don't modify existing code, add new code.

3. Liskov Substitution Principle -
   - Derived classes must be usable through the base class interface, without the need for the user to know the differences.
   - Client should not know which specific subtype they are calling.
   - It is an extension of Open/Closed Principle.
   - Any new functionality should be implemented by adding new classes, attributes and methods, instead of changing the current ones or existing ones.

4. Interface Segregation Principle (ISP) -
   - No client should be forced to depend on methods it does not use.
   - One fat interface need to be split to many smaller and relevant interfaces so that clients can know about the interfaces that are relevant to them.
  
5. Dependency Inversion Principle (DIP) -
   - High-level modules should not depend on low-level modules. BOth should depend on abstractions.
   - Abstractions should not depend on details. Details should depend on abstractions.
