# Comparison operators 
### Evaluating conditions

You can evaluate a situation by comparing one value in the script to what you expect it might be. The result will be a boolean: True or False.

- `==` is equal to. Compares two values (numbers, strings, booleans)
- `!=` is not equal to. 
- `===` strict equal to. Check that both data type and value are the same.
- `!==` strict not equal to.  Check that both data type and value are not the same.
- `>` greater than
- `<` less than
- `>=` greater than or equal
- `<=` less than or equal

We call this testing or checking **evaluating the condition**.

# Logical operators

Logical operators allow you to compare the results of more than one comparison operator.

- `&&` **logical and**. Test more than one condition
`((2 < 5) && (3 >=2))` returns true. If both of the expressions evaluate then the expression returns true. All else will return false. 

- `||` **logical or**. Test at least one condition. 
`((2 < 5) || (2 < 1))` returns true. If at least one of the expressions evaluates true, it will return true. It will return false only if all expressions evaluate false.

- `!` **logical not**. Takes a single boolean and inverts it. `!(2 < 1)` returns true.


# Loops

Loops check a condition. If it returns true, a code block will run. It repeats until the condition returns false. 

3 types of loops:
- **FOR** if you need to run code a specific number of times.
- **WHILE** code will continue the loop for as long as the condition is true.
- **DO WHILE** will run the statements inside the curly brackets at least once even if the condition evaluates false.

`for (var i = 0; i < 10; i++) {
document.write(i);
}`

`(var i = 0; i < 10; i++)` is the condition counter
`document.write(i);` is the code to execute during loop (between the curly brackets).

## Loop counter

A **for** loop uses a counter as a condition. This instructs the code to run a specified amount of times.

Condition is made of 3 statements:
- **initialization**. Create a variable and set it to 0 `var i = 0;`
- **condition**. The loop should continue until the counter reaches a specified number `i < 10;`
- **update**. Everytime the loop runs, it adds one to the counter `i++`

A **while** loop will continue to run as long as the condition in the parenthesis are true.
`while (i < 10)`