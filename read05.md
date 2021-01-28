# Comparison, logical operators and Loops 

## Comparison

Comparison operators are used in logical statements to determine equality or difference between variables or values.

#### The table below explains the comparison operators:

![](https://i.ytimg.com/vi/wFB-ywsNPwg/maxresdefault.jpg)


## logical operators

Logical operators are used to determine the logic between variables or values.

#### The table below explains the logical operators:

![](https://slideplayer.com/slide/15945194/88/images/25/Logical+Operators+%28cont.%29.jpg)


## Loops

Loops are handy, if you want to run the same code over and over again, each time with a different value.

### For loop
  
loops through a block of code a number of times.

**Syntax**

`for (statement 1; statement 2; statement 3) { // code block to be executed }`

- *Statement 1*: is executed (one time) before the execution of the code block.

- *Statement 2*: defines the condition for executing the code block.

- *Statement 3*: is executed (every time) after the code block has been executed.

**Example**
`for (i = 0; i < 5; i++) { text += "The number is " + i + "<br>"; }`


### While loop

The while loop loops through a block of code as long as a specified condition is true.

**Syntax**

`while (condition) { // code block to be executed }`

**Example**

In the following example, the code in the loop will run, over and over again, as long as a variable (i) is less than 10:

`while (i < 10) { text += "The number is " + i; i++;}`

*If you forget to increase the variable used in the condition, the loop will never end. This will crash your browser.*