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
that superclass: `SuperClass sc = new SubClass1();`

## Using super


### Using super to Call Superclass Constructors

### A Second Use for super
















## Overloading Vararg Methods

You can overload a method that takes a variable-length argument.
Two ways that a varargs method can be overloaded:
- First, the types of its vararg parameter can differ.
- The second way is to add one or more normal parameters.

<hr />

**NOTE:** A varargs method can also be overloaded by a non-varargs method. For example, `vaTest(int x)` is a
valid overload of `vaTest(int... v)`. This version is invoked only when one `int` argument
is present. When two or more `int` arguments are passed, the varargs version `vaTest(int... v)` is used.

## Varargs and Ambiguity

First Example:

- `static void vaTest(int... v) { // ...`
- `static void vaTest(boolean... v) { // ...`
- Call to `vaTest(); // Error: Ambiguous!`

<hr />

Second Example:

- `static void vaTest(int... v) { // ...`
- `static void vaTest(int n, int... v) { // ...`
- Call to `vaTest(1); // Error: Ambiguous!`

<hr />

**Solution:** Forego overloading and simply use two different method names.
