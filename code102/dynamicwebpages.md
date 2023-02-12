# How do I write a script for a web page?

JS is the behavior layer. This is where you add the interactivity.

As good practise, link your JS file at the end of the body in your HTML sheet so it won’t affect too much the loading time for the rest of the info on your site.
Use this element : `<script src=”yourfile.js”></script>`

## Calling the method of an object 

`document.write(‘Good afternoon’);`

- Document is the object
- . is the member operator
- write() is the method of the object
- ‘Good afternoon’ is the parameter of the method. This is the piece of info that is going to be displayed.


# Basic JS instructions

> JS is case sensitive.

Write comments to explain what your code is doing:
- `//` for single line comments
- `/*your comment*/` for multi line comments

Each individual instruction or step is called a **Statement**. It ends with ; (tells that the step is over).
`var today = new Date();`

Code block is a statement surrounded by { }

### What is a variable?

A variable stores data temporarily to perform the job. This data will change every time the script runs.
  - Create a variable and give it a name: `var name;`. **var** is the variable keyword, **name** is the variable name. This process is called **declare a variable**.
- Assign value: `name = “lulu”;`. = is called the assignment operator.
- You can change the value of a variable later in the same script by using the variable name and assign a new value. `name = “ludi”;`

Data types:
- Numeric date type
- String data type (letters and other characters)
- Boolean data type (true or false)