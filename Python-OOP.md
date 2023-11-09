# Object Oriented Programming in Python

- Python supports all different programming paradigms-
  1. Functional Programming
  2. Object Oriented Programming 
  3. Procedural Programming
- In OOP everything revolves around Classes & Objects.
- A class is a blueprint of an object. And a object is a instance of a class.
- Every object of a class has certain proberties/attributes and behavior/methods.
- Objects are stored in heap memory of system. And every object have a unique-ID.
- Size of an object depends on the number of variables declared in it.

## Special method :
```python
def __init__(self):
    # Your code here
```

- When we define 'init' method in a class, it will be called automatically when object (of the class) is created.
- 'init' is like a constructor who initializes variables of object and allocates size to object.
- Here 'self' refers to calling object itself.

## Variables : 
-  In Python, variables can be defined as attributes that are associated with a particular class or instance of a class.
-  Types of variables:
   1. Static/Class variables.
   2. Instance variables.
- Static/Class variables - These variables are shared by all instances of a class. They are defined within the class but outside of any class methods. Class variables are typically used to define attributes that are common to all instances of the class.
- Instance variables: These variables are unique to each instance of a class. They are defined within the class methods, usually within the __init__ method. Instance variables are used to store data that is specific to each instance of the class.
```python
class MyClass:
    class_variable = 0

    def __init__(self, instance_variable):
        self.instance_variable = instance_variable
```

## Methods :
- In python, methods are functions that are defined within a class and are used to define the behavior of objects.
- Types of methods:
  1. Instance Methods
     - Accessor Methods (getters).
     - Mutator Methods (setters).
  2. Class Methods.
  3. Static Methods.

- Instance Methods - These are the most common type of method and are used to define the behavior of an object. Instance methods must have at least one parameter, usually named self, which refers to the instance that the method is being called on.
  ```python
  class MyClass:
    def instance_method(self, arg1, arg2):
        # method logic using self and arguments
        pass
  ```

- Class Methods - These methods are used to work with class-level data (means common to whole class). They are defined using the @classmethod decorator and take a parameter commonly named cls, which refers to the class itself. Class methods can be used to create factory methods or manipulate class-specific variables.
  ```python
  class MyClass:
    class_variable = 0

    @classmethod
    def class_method(cls, arg1, arg2):
        # method logic using cls and arguments
        pass
  ```

- Static methods -
   - This method has nothing to do with class and instance variables.
   - They are defined using the @staticmethod decorator and do not require any specific parameters like self or cls.
   - We use them when we want to perform any operation on other class objects or to perform some operations like factorial, etc.
  ```python
  class MyClass:
    @staticmethod
    def static_method(arg1, arg2):
        # method logic without using self or cls
        pass
  ```

## Inner Class
- In Python, an inner class is a class that is defined within the scope of another class. It is a way of logically grouping classes that are only used in one place. Inner classes are used to encapsulate and organize related classes within a larger class.
- We can create objects of inner class inside the outer class and outside outer class also provided the use of outer class name to call it.
```python
class OuterClass:
    def __init__(self):
        self.inner = self.InnerClass()

    class InnerClass:
        def inner_method(self):
            print("This is an inner method.")

# Creating an instance of the outer class
outer_obj = OuterClass()

# Accessing the inner class and its method
outer_obj.inner.inner_method()
```

## Inheritance
- Inheritance is a fundamental concept in object-oriented programming (OOP) that allows a new class (the derived or child class) to inherit properties and behaviors from an existing class (the base or parent class), with the ability to reuse code and extend the functionality of the base class.
- Types of Inheritance:
  1. Single.
  2. Multiple.
  3. Multilevel.

## Polymorphism
- Polymorphism refers to making multiple functions with the same name having difference in number of parameters and datatypes.
- Types of polymorphism:
  1. Duck Typing.
  2. Operator overloading.
  3. Method overloading and overriding.

  
