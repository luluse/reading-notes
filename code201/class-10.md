# Error Handling & Debugging

##JavaScript book, Ch. 10, “Error Handling & Debugging”

execution context:
- global context
- function context
- eval context

#### Error objects
- error: generic error
- SyntaxError
- ReferenceError: tried to reference a variable that is not declared/within scope
- TypeError: an unexpected data type that cannot be coerced
- Range Error: number outside of range
- URIError
- EvalError

#### Console.log methods
- `console.info()` can be used for general info
- `console.warn()` can be used for warnings
- `console.error()` can be used to hold errors
- `console.group()` to write a set of related data
- `console.table()` output a table showing objects/arrays that contain other objects or arrays
- `console.assert()` to test if a condition is met

you can pause the execution of a script on any line using **breakpoint** and check the values stored in variables at that point in time.

#### Debugger keyword in JS
When placing the **debugger** keyword in your script, it will automatically create a breakpoint when opening the console. 

#### Throwing errors

If you know something might cause a problem for your script you can generate your own errors before the interpretor creates them.

` throw new Error('message');`

#### Debugging tips
- try code in another browser
- write numbers in the console to see how far your code runs
- remove parts of your code, comment out until finding the items generating errors
- explain the code out loud to someone else
- search
- validation tools


