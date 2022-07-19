---
sidebar_position: 1
---

# Varargs: Variable-Length Arguments

[//]: # (SHOULD BE COMPLETE)

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
