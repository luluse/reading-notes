# Classes, Inheritance, Functional Programming

#### Name 3 advantages to Test Driven Development

1. provides the immediate feedback on the developed components. Easier to find bugs

2. maximizes the possibility of developing the best quality product fulfilling the communicated needs of clients.

3. helps to create better modularized, extensible and flexible code. Test Driven Development approach drives the Agile team to plan, develop and test the small units to be integrated at advanced stage. Under this approach, the concerned member delivers and performs better because of being more focused on smaller unit. 

- [knowledgehut](https://www.knowledgehut.com/blog/agile/6-compelling-benefits-of-tdd-test-driven-development#:~:text=TDD%20helps%20to%20create%20better,more%20focused%20on%20smaller%20unit.)

#### In what case would you need to use beforeEach() or afterEach() in a test suite?

If you have some work you need to do repeatedly for many tests, you can use beforeEach and afterEach. they run for every it() block.

- [jestjs](https://jestjs.io/docs/en/setup-teardown)
- [Github](https://github.com/pester/Pester/wiki/BeforeEach-and-AfterEach)

#### What is one downside of Test Driven Development.

Maintaining the test code along with your production code. Time consuming.

- [Stackoverflow](https://stackoverflow.com/questions/64333/disadvantages-of-test-driven-development)

#### What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

ES6 Classes are easier to read and work with. The main difference is the syntax.

- [medium](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

#### Name a use case for a static method

static methods are used to implement functions that belong to the class, but not to any particular object of it.

- [JavaScript.info](https://javascript.info/static-properties-methods)

#### Write an example of a Higher Order function and describe the use case it solves
```
users = [
  {
    name: 'Yazeed',
    age: 25
  },
  {
    name: 'Sam',
    age: 30
  },
  {
    name: 'Bill',
    age: 20
  }
];

namesStartingWithB = users.filter((user) => startsWithB(user.name));

console.log(namesStartingWithB);
```

Great reusability, allows for functions that operate on other functions.

- [free code camp](https://www.freecodecamp.org/news/a-quick-intro-to-higher-order-functions-in-javascript-1a014f89c6b/)

#### functional programming

Functional programming is the process of building software by composing pure functions, avoiding shared state, mutable data, and side-effects. It contrast with object oriented programming.

- [Medium](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-functional-programming-7f218c68b3a0)

#### pure function

A function must pass two tests to be considered “pure”:Same inputs always return same outputs and no side-effects.

- [Free code camp](https://www.freecodecamp.org/news/what-is-a-pure-function-in-javascript-acb887375dfe/)

#### higher-order function

A function that accepts and/or returns another function.You can use it as a piece of data. The greatest benefit of HOFs is greater reusability.

- [Free code camp](https://www.freecodecamp.org/news/a-quick-intro-to-higher-order-functions-in-javascript-1a014f89c6b/)

#### immutable state

 An immutable object, is an object whose state cannot be modified after it is created.string and numbers are immutable data types.
 Keeping the state immutable can help you in terms of performance, predictivity and better mutation tracking.

 - [dzone](https://dzone.com/articles/immutability-in-javascriptwhy-and-when-should-you)

#### object

OBject is a datatype. It is used to store various keyed collections and more complex entities.

- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

#### object-oriented programming (OOP)

Use objects to model real world things that we want to represent inside our programs, and/or provide a simple way to access functionality that would otherwise be hard or impossible to make use of.
- [MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Object-oriented_JS)


#### class

Classes are "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations.
- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)


#### prototype
Prototype property is basically an object (also known as Prototype object), where we can attach methods and properties in a prototype object, which enables all the other objects to inherit these methods and properties.

- [Geeks for Geeks](https://www.geeksforgeeks.org/prototype-in-javascript/)


#### super
The super keyword is used to access and call functions on an object's parent.
- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)


#### inheritance

"child" object classes (constructors) inherit features from their "parent" classes.
- [MDN](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Inheritance)

#### constructor

A constructor enables you to provide any custom initialization that must be done before any other methods can be called on an instantiated object.

-[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/constructor)

#### instance
Instance properties must be defined inside of class methods
In JavaScript, "instance" does not have a technical meaning because JavaScript does not have this difference between classes and instances. However, in talking about JavaScript, "instance" can be used informally to mean an object created using a particular constructor function. 
- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Details_of_the_Object_Model#:~:text=In%20JavaScript%2C%20%22instance%22%20does,using%20a%20particular%20constructor%20function.)

#### context
if you just type this in the console, you will get the window-object, the outermost context for your JavaScript.
Context only makes sense inside of functions.
- [Free code camp](https://www.freecodecamp.org/news/how-to-understand-the-keyword-this-and-context-in-javascript-cd624c6b74b8/)

#### this

reference to the instance that you created.

- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

#### Test Driven Development (TDD)

approach of programming by coding, testing (writing unit tests) and designing (refactoring)

- [knowledgehut](https://www.knowledgehut.com/blog/agile/6-compelling-benefits-of-tdd-test-driven-development#:~:text=TDD%20helps%20to%20create%20better,more%20focused%20on%20smaller%20unit.)

#### Jest

JavaScript Testing Framework
- [jestjs](https://jestjs.io/docs/en/setup-teardown)

#### Continuous Integration (CI)

Continuous Integration (CI) is the process of automating the build and testing of code every time a team member commits changes to version control.
- [Azure DevOps](https://docs.microsoft.com/en-us/azure/devops/learn/what-is-continuous-integration)

#### unit test
Unit tests only test a single part of your implementation. A unit. No dependencies or integrations, no framework specifics. They're like a method that returns a link in a specific language:
- [Free cpode camp](https://www.freecodecamp.org/news/how-to-start-unit-testing-javascript/)
