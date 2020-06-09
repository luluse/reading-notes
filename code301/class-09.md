# Refactoring

## Concepts of Functional Programming in Javascript

> “Complexity is anything that makes software hard to understand or to modify." — John Outerhout

**Pure functions:** 
- It returns the same result if given the same arguments
- If our function reads external files, it’s not a pure function — the file’s contents can change.
- Any function that relies on a random number generator cannot be pure

**Pure functions are stable, consistent, and predictable.**

**Immutability:**
- When data is immutable, its state cannot change after it’s created.

**Referential transparency:**

- pure functions + immutable data = referential transparency

**Functions as first-class entities:**
- refer to it from constants and variables
- pass it as a parameter to other functions
- return it as result from other functions

The idea is to treat functions as values and pass functions like data.

**Higher-order functions:**
- takes one or more functions as arguments, or
- returns a function as its result

**Filter:**

Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. 

`const even = n => n % 2 == 0;`

`const listOfNumbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10];`

`listOfNumbers.filter(even); // [0, 2, 4, 6, 8, 10]`

**Map:**

The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.

- transform a given array into a new array

**Reduce:**

The idea of reduce is to receive a function and a collection, and return a value created by combining the items.

## Refactoring JavaScript for Performance and Readability

- Return early from functions
- Cache variables so functions can be read like sentences
- Check for Web APIs before implementing your own functionality
