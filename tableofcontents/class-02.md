# Text

Structural Markup: Elements that you can use to describe both headings and paragraphs.

Semantic markup: provides extra information to the page without affecting its structure.

Headings: 6 levels of headings.
- `<h1>`This is the largest heading`</h1>`
- `<h6>`This is the smallest heading`</h6>`

Paragraphs: `<p>`The start of a paragraph is indicated by a new line`</p>`


- `<b>`Makes characters appear bold`</b>`
- `<strong>`Indicates that this content has strong importance. By default, it will appear bold`</strong>`
- `<i>`Indicates emphasis. By default, it will appear italic`</i>`
- `<em>`Makes characters appear italic`</em>`
- Superscript: `4<sup>th</sup> of September`
- Subscript: `CO<sub>2</sub>`
- Line break `<br/>`
- Horizontal rule break `<hr/>`
- `<blockquote>`Used for long quotes that take up an entire paragraph. It will indent the content`</blockquote>`
`<q>`Used for shorter quotes that sit within a paragraph`</q>`
- Abbreviations & Acronyms: `<abbr title=”National Aeronautics and Space Administration”>NASA</abbr> ` When hovering, it gives the acronym description.

# Introducing CSS

Css works like an invisible box around every HTML element. It allows you to create rules that control the way that each individual box is presented.

- Css works by associating rules with HTML elements. A CSS rule contain two parts:

`P {font-family: Arial;}` where `P` is the selector and `{font-family: Arial;}’ is the declaration.

- a CSS declaration contain a property and a value separated by a colon :

`{font-family: Arial;}’ where font-family is the property and Arial is the value.

### How to link you CSS sheet to your HTML sheet :

`<link href=”css/style.css” type=”text/css” rel=”stylesheet” />` This element lives inside the head of your HTML sheet.

### Commonly used selectors:

- Universal selector * {} Targets all elements on the page
- Class selector .note {} Targets any element whose class attribute has a value of note.
- ID selector #introduction {} Targets elements whose id attribute has a value of introduction.

### Advantages to place CSS rules in a separate style sheet:

- All of your web pages can share the same style sheet
- Website will load faster
- Easier to edit and update
- Good practice, keeps HTML sheet easier to read


# Basic Javascript Instructions

A **statement** is an individual instruction that ends with a semicolon (tells that the step is over). Each statement start on a new line.

Statements can be organized in code blocks. They are surrounded by curly brackets.

> JS is case sensitive.

Write comments to explain what your code is doing:

- `/* Multi line comment */`
- `// single line comment`

Data types:

- Numeric date type
- String data type (letters and other characters)
- Boolean data type (true or false)

**Escaping technique** : use a backslash before a quote mark that appears in a string. Tells the interpreter the following character is part of the string.

Creating variables:
- variables are declared an d values assigned in the same statement. 
`var name = lulu`
- several variables are declared on the same line, then values assigned to each.
`var name, username;
name = lulu;
username = luluse;`

> You can change the value of a variable later in the same script. Use the variable name and assign it a new value.

Rulesfor naming variables: 
- must start with a letter, $ or _
- Can't use - and . in a variable name
- can't use keywords or reserved words
- Variables are case sensitive
- Use a name that describes the kind of info that the variable stores.
- If name is made up of several words, use a capital letter for the first letter of every word. 

### Arrays

Stores a list of values related to each other. Values are assigned to the array inside a pair of square brackets, each value is separated by a comma. Values don't need to be the same date type.

Values are accessed as if they are a numbered list that starts at **Zero**. Each value is given a number called an **Index**. 

### Expressions

An expression result in a single value. There are 2 types o expression:
- expressions that just assign a value to a variable
- expressions that use two or more values to return a single value

### Operators

Expressions rely on operators. They allow to create a single value from one or more value.
- Assignment operator =
- Arithmetic operators: perform basic maths
- String operators: combine two strings
- Comparison operators: compare two values and return true or False
- Logical operators: combine expressions and return true or false 

# Decisions and Loops

### Decision making

There are several places in a script where decisions are made that determine which line of code should run next. Set a **condition** in order to determine which path to take.

### Evaluation conditions and conditional statements

- Evaluation of a condition: compares two values and return true of false.
- Conditional statement is based on a concept of if/then/else.

### Evaluating conditions
You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a boolean: True or False.

- == is equal to. Compares two values (numbers, strings, booleans)
- != is not equal to.
- === strict equal to. Check that both data type and value are the same.
- !== strict not equal to. Check that both data type and value are not the same.
- > greater than
- < less than
- >= greater than or equal
- <= less than or equal

We call this testing or checking evaluating the condition.

### Comparison operators

In any condition there is one **operator** and two **operands**. They can be values or variables.

### Logical operators

Logical operators allow you to compare the results of more than one comparison operator.

- `&&` logical and. Test more than one condition `((2 < 5) && (3 >=2))` returns true. If both of the expressions evaluate then the expression returns true. All else will return false.

- `||` logical or. Test at least one condition. `((2 < 5) || (2 < 1))` returns true. If at least one of the expressions evaluates true, it will return true. It will return false only if all expressions evaluate false.

- `!` logical not. Takes a single boolean and inverts it. `!(2 < 1)` returns true.

### If statement

Evaluates a condition. if the condition evaluates to **true**, statements in the code block are executed.

# Git commit message 

- Capitalize the subject line
- Do not end line with a period
- Limit the subject line to 50 characters
- Use the imperative mood in the subject line