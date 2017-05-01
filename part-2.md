# Part Two

## Higher-Order Functions
* In Functional Programming, a function is a first-class citizen of the language. In other words, a function is just another value.
* Higher-order Functions either take functions as parameters, return functions or both.
* Higher-Order Functions value scope behavior is called a closure.

## Closures
* A closure is a function's scope that's kept alive by a reference to that function.
* Closures are problematic since the variables are mutable, they can change values from the time they were closed over to the time the returned function is called.
* Variables in Functional Languages are Immutable eliminating this common source of bugs and confusion.

## Code
### Code one
```
validateSsn = ssn =>
    /^\d{3}-\d{2}-\d{4}$/.exec(ssn)
    ? console.log('Valid SSN')
    : console.log('Invalid SSN')

validatePhone = phone =>
    /^(\d{3})\d{3}-\d{4}$/.exec(phone)
    ? console.log('Valid Phone Number')
    : console.log('Invalid Phone Number')
```

### Code two
```
validateValue = (value, regex, type ) =>
    regex.exec(value)
    ? console.log('Valid ' + type)
    : console.log('Invalid ' + type)
```

### Code three
```
validateValueWithFunc = (value, parseFunc, type)
    parseFunc(value)
    ? console.log('Valid ' + type)
    : console.log('Invalid ' + type)
```

### Code four
```
makeRegexParser(regex) => regex.exec
validateValueWithFunc = (value, parseFunc, type)
    parseFunc(value)
    ? console.log('Valid ' + type)
    : console.log('Invalid ' + type)
```

### Code five
A higher-order function that returns a function:
```
makeAdder = constantValue => value => constantValue + value
```
