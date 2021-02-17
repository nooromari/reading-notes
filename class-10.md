## HANDLING & DEBUGGING

- If you understand **execution contexts** (which have two stages) and stacks, you are more likely to find the error
in your code.

Every statement in a script lives in one of three execution contexts:

1. **GLOBAL CONTEXT**
Code that is in the script, but not in a function.There is only one global context in any page.
2. **FUNCTION CONTEXT**
Code that is being run within a function. Each function has its own function context.
3. **EVAL CONTEXT** (NOT SHOWN)
Text is executed like code in an internal function called eval().


**VARIABLE SCOPE**

1. **GLOBAL SCOPE**: If a variable is declared outside a function, it can be used anywhere because it has global scope. The `var` keyword create a variable in global scope.

2. **FUNCTION-LEVEL SCOPE**: When a variable is declared within a function,
it can only be used within that function. 


- Debugging is the process of finding errors. It involves a process of deduction.



![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/08/JavaScript-Debugging-and-Testing.png)



- The console helps narrow down the area in which the error is located, so you can try to find the exact error. The `console.log()` method can write data from a script to the console. If you open console-log.html, you will see that a note is written to the console when the page loads. And you can use three different methods:

1. `conso1e.info()` can be used for general information.
2. `console.warn()` can be used for warnings.
3. `console.error()` can be used to hold errors.


- JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.

   1. Syntax Error: This is caused by incorrect use of the rules of the language. It is often the result of a simple typo.
   2. Reference Error: This is caused by a variable that is not declared or is out of scope.
   3. URI Error: If these characters are not escaped in URls, they will cause an error: / ? & I : ;
   4. Type Error: This is often caused by trying to use an object or method that does not exist.
   5. RangeError: If you call a function using numbers outside of its accepted range.
   6. NaN *(NOT A NUMBER)*: If you perform a mathematical operation using a value that is not a number, you end up with the value of NaN, not a type error.
   7. EvalError: INCORRECT USE OF eval() FUNCTION.

- You can create a breakpoint in your code using just the debugger keyword. When the developer tools are open, this will automatically create a breakpoint.

- If you know that you may get an error, you can handle it gracefully using the **try**, **catch**, **finally** statements. Use them to give your users helpful feedback.
