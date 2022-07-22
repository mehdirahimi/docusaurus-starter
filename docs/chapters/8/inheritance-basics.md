---
sidebar_position: 1
---

# Inheritance


## Inheritance Basics

- In the terminology of Java, a class that is inherited is called a **superclass**.
- The class that does the inheriting is called a **subclass**.
- **Subclass** includes all the members of its **superclass**.
- Java does not support the inheritance of multiple superclasses into a single subclass.
- No class can be a superclass of itself.

### Member Access and Inheritance
### A More Practical Example
### A Superclass Variable Can Reference a Subclass Object

A reference variable of a superclass can be assigned a reference to any subclass derived from
that superclass:
- `SuperClass sc = new SubClass1();`

## Using super

`super` has two general forms:
- Calls the superclass’ constructor.
- Access a member of the superclass that has been hidden by a member of a subclass.

### Using super to Call Superclass Constructors

- When a subclass calls `super()`, it is calling the constructor of its immediate superclass.
- `super()` must always be the first statement executed inside a subclass’ constructor.
- We are able to pass **SubClass** object to the **SuperClass** constructor.

### A Second Use for super

- Using super to overcome **name hiding** (acts somewhat like `this`).

## Creating a Multilevel Hierarchy
## When Constructors Are Executed

- In a class hierarchy, constructors complete their execution in order of derivation, from superclass to subclass.

## Method Overriding

- When a method in a subclass has the **same name** and **type signature** as a method in its superclass.
- You cannot override a method and reduce visibility.

[//]: # (- You cannot override a method and change return type.)

- The overriding method must obey the following rules:
  - `final` and `static` methods cannot be overridden.
  - The overriding method must have same argument list.
  - The overriding method must have same return type (or subtype).
  - The overriding method must not have more restrictive access modifier:
    - If the overridden method is:
      - `default`, then the overriding one must be `default`, `protected` or `public`.
      - `protected`, then the overriding one must be `protected` or `public`.
      - `public`, then the overriding one must be only `public`.
  - The overriding method must not throw new or broader **checked** exceptions.
    - The overriding method may throw fewer or narrower checked exceptions, or **any** unchecked exceptions.
  - Use the `super` keyword to invoke the overridden method from a subclass.
    - It’s very common that a subclass extends a superclass’ behavior rather than re-implementing the behavior from scratch.
  - Constructors cannot be overridden.
  - 