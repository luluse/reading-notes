# The Call Stack and Debugging

### [The Call stack defined on MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)

> mechanism for an interpreter to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.

### [Understanding the JavaScript call stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

- The call stack is primarily used for function invocation (call)
-  the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It is single-threaded. Meaning it can only do one thing at a time.
- the call stack is synchronous. It maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). 
- data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call)
- Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack
- A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point.

### [JavaScript error messages && debugging](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

Types of error messages:
- Reference errors: when you try to use a variable that is not yet declared you get this type os errors. Also a common thing when using const and let.
- Syntax errors: this occurs when you have something that cannot be parsed in terms of syntax, like when you try to parse an invalid object using JSON.parse.
- Range errors: Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
- Type errors: show up when the types (number, string and so on) you are trying to use or access are incompatible.

Debugging:
- the most common way its to simply console.log() the variables you want to check
- chrome developer tools, create a break point
- debugger statement in your code

Tools to avoid runtime errors:
- quokka to evaluate your code as you type
- eslint
