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

ES6 Classes are easier to read and wokr with. The main difference is the syntax.

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

usernames = users.map(getName);

console.log(usernames);
```

#### functional programming

#### pure function

#### higher-order function

A function that accepts and/or returns another function.You can use it as a piece of data. The greatest benefit of HOFs is greater reusability.

- [Free code camp](https://www.freecodecamp.org/news/a-quick-intro-to-higher-order-functions-in-javascript-1a014f89c6b/)

#### immutable state

#### object

#### object-oriented programming (OOP)

#### class

Classes are "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations.
- [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)


#### prototype

#### super

#### inheritance

#### constructor

#### instance

#### context

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

#### unit test