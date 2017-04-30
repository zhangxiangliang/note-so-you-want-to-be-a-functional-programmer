# Part Two

## Higher-Order Functions
* In Functional Programming, a function is a first-class citizen of the language. In other words, a function is just another value.
* Higher-order Functions either take functions as parameters, return functions or both.
* Higher-Order Functions value scope behavior is called a closure.

## Closures
* A closure is a function's scope that's kept alive by a reference to that function.
* Closures are problematic since the variables are mutable, they can change values from the time they were closed over to the time the returned function is called.
* Variables in Functional Languages are Immutable eliminating this common source of bugs and confusion.
