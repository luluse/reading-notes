# Programming with JavaScript


JavaScript allows to make web pages more interactive in 4 ways:
- Access the content of the page
- Modify the content of the page
- Program rules and instructions
- React to events 

### What is a script?

A serie of instructions that computer can follow to achieve a goal.

To write a script you need to state your goal and list the tasks that need to be completed in order to achieve it:
- Define the goal
- Design the script (write down each individual steps the computer needs to perform)
- Code each step



## Expressions + Operators

An **expression** results in a single value. There are two types of expression:
- expression that just assign a value to a variable `car color = blue ;`
- expression that use two or more values to return a single value `var area = 3 * 2 ;`

Expressions rely on **operators**. They allow programmers to create a single value from one or more values. 

### Arithmetic operators

- Addition +
- Subtraction -
- Division /
- Multiplication * 
- Increment ++ (adds 1 to the current number)
- Decrement -- (Subtracts one from the current number)
- Modulus % (Divides two values and returns the remainder)

### String operators

There is one sting operator: + It joins the strings side by side. This is called **concatenation**.


If you use any of the other arithmetic operators on a string you will result with a value `NaN` (Not a Number). 


## Functions

Functions let you group a series of statements together to perform a specific task, they’re packed in a **code block**. 

When you ask a function to perform its task, it is known as **calling** the function.

Pieces of information passed to a function are called **parameters**.

When you write a function, you expect an answer, the response is called a **return value**.

### Declaring a function

`function sayHello() { Document.write(‘Hello!’); }`

- **function** is the function keyword
- **sayHello()** is the function name
- The code block is between the curly brackets

### Calling a function 
When a function is declared, you can use it several times in your code to perform the same task by typing the **function name** where you need it.
`sayHello();`

> Declare the function before calling it.

### Declaring a function that needs information

When you declare a function you give it **parameters**. Inside the function, the parameters act like **variables**. 

`function getArea(width,height) {
	Return width * height;
}`

Each time you call the function, the values could be different.

When you call a function that has parameters, you specify the values it should use in the parentheses that follow the name. The values are called **arguments**. They can be values or variables.  

- arguments as values:
`getArea(3, 5);`
- arguments as variables:
`wallWidth = 3;
wallHeight = 5;
getArea(wallWidth, wallHeight);`