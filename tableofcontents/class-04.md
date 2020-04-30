## HTML Links

Links are created using the `<a href=""></a>` element. The text between the opening and closing tag is called **link text**.

Linking to other websites: the value of the href attribute will be the full web address for the site. it is known as **absolute** URL.

Linking to other pages on the same site: use the **relative** URL. The href attribute is just the name of the file if all the pages are in the same folder.
- same folder: use fileName.html
- child folder: use nameOfTheChildFolder/fileName.html
- grandchild folder: use childFolder/grandChildFolder/fileNAme.html
- parent folder: use ../FileName.html
- grandparent folder: use ../../fileName.html

Email links:
- `<a href="mailto:lulu@gmail.com">Email Lulu</a>`

opening links to a new window:
- add attribute `target=_blank` in the `<a>` tag.

Linking to a specific part of same page:
- add list of contents at the top of page
- add an Id attribute to sections you want to link.

## CSS Layout

### Positionnning elements

#### Building blocks

CSS treats each HTML element as if it is in its on box:

- block level box: start on a new line and acts like the main builing block. `<h1>` `<p>` `<ul>` `<li>`
- inline box: flow between surrounding text. `<img>` `<i>` `<b>`

#### Containing elements

If one block-level element sits inside another block-level element, the outert box is known as the **containing** or **parent** element.
It is common to group a number of elements together inside a `<div>` element

#### Controlling the position of elements

- **Normal flow**. Every block-level appears on a new line. Each item appears one after another vertically down the page. 
- **Relative positioning**. Moves an element from the position it would be in normal flow.
- **Absolute positioning**. Positions the element  in relation to its containing element.
- **Fixed positioninig**. Position the element in relation to the browser window. Elemeont do not move when the user scrolls up and down.
- **Floating elements**. Allows to take tha element out of normal flow and position it to the far left or far right of a containing box. Becomes a block-level element where other content can flow around. Always use the width property to indicate how wide the floated element should be.

If boxes overlap, `z-index` property allows you to control which box appears on top. 

To indicate where a box should be positioned, you can use **box offset** properties and tell the browser how far from top/bottom/left/right it should be placed. Properties are usually given in px, percentages or ems.

## JS Functions


Functions let you group a series of statements together to perform a specific task, they’re packed in a **code block**.

When you ask a function to perform its task, it is known as **calling** the function.

Pieces of information passed to a function are called **parameters**.

When you write a function, you expect an answer, the response is called a **return value**.

#### Declaring a function

`function sayHello() { Document.write(‘Hello!’); }`

- **function** is the function keyword
- **sayHello()** is the function name
- The code block is between the curly brackets

#### Calling a function

When a function is declared, you can use it several times in your code to perform the same task by typing the **function name** where you need it. `sayHello();`

> Declare the function before calling it.

#### Declaring a function that needs information

When you declare a function you give it **parameters**. Inside the function, the parameters act like **variables**.

`function getArea(width,height) { Return width * height; }`

Each time you call the function, the values could be different.

When you call a function that has parameters, you specify the values it should use in the parentheses that follow the name. The values are called **arguments**. They can be values or variables.

arguments as values: `getArea(3, 5);`
arguments as variables: `wallWidth = 3; wallHeight = 5; getArea(wallWidth, wallHeight);`

#### Getting a single value out of a function

Some functions return information to the code that called them. For example, when they perform a calculation, they return the result. The same function can be used to perform the same steps with different values.

#### Getting multiple values out of a function

Functions can return more than one value using an array. 

#### Anonymous functions & function expressions
 
A **function declaration** created a function that you can call later in your code.
`function area(width, height){return width * height;}`
`var size = area()`

In **function expressions**, the name is usually ommited. A function with no name is called an **anonymous function**.
`var area = function(width, height){ return width * height;}`
`var sie = area(3, 4);`

#### Immediately invoked function expressions

**IIFE**

These functions are note given a name. They're are executed once as the interpreter comes accross them. They're used for code that only needs to run once within a task.

#### Variable scope

The location where you declare a functions will affect where it can be used within your code. This is called as the **variable's scope**.

- Local variables are created inside a function and can only be used in that function.
- Global variables are created outside of a function and can be used anywhere within the script.

## 6 reasons for pair programming

Pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing. The Driver manages the text editor, switching files, version control, writing code, thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs.

- Greater efficiency. Easier to catch mistakes, come up with solutions faster.
- Engaged collaboration. harder to procrastinate or get off tracks. 
- Learning from fellow students. Everyone brings a unique approche to a specific problem, everyon has different skill sets. 
- Social skills. learn how to work with others.
- Job interview readiness. 
- Work environment readiness. 