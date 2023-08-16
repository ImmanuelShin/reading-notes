# Operators and Loops

## Expressions

A valid unit of code that resolves to a value. Expressions fall largely into two types:

- Those with side effects (such as assigning values).
- Those that purely evaluate.

`x = 7` is an example of the first type. This expression assigns the value of 7 to the variable x.

`3 + 4` is an example of the second type. This expression solely evaluates the sum of 3 and 4. In this example, the expression is essentially useless unless it is tacked on to a larger construct (e.g `x = 3 + 4`).

## Loops

Loops are reiterable blocks of code. They are useful for repeating actions to a specified number of times (sometimes an infinite amount).

There are a multitude of loops provided in JavaScript:

- for statement:
  > for (let i = 0; i < someNumber; i++){  
  > &nbsp;&nbsp;code;  
  > }  
- do...while statement:
  > let i = 0;  
  > do {  
  > &nbsp;&nbsp;i++;  
  > &nbsp;&nbsp;code;  
  > } while (i < someNumber);  
- while statement:
  > let n = 0;  
  > while (n < someNumber) {  
  > &nbsp;&nbsp;n++;  
  > &nbsp;&nbsp;code;  
  > }
- labeled statement:
  - Labeling a statement.
  > labelWhileLoop: while (true) {  
  > &nbsp;&nbsp;code;  
  > }  
- break statement:
  - Lets you terminate a loop. Can be used in conjunction with a labeled statement.
  > labelWhileLoop: while (true) {  
  > &nbsp;&nbsp;code;  
  > &nbsp;&nbsp;if (true) {  
  > &nbsp;&nbsp;&nbsp;&nbsp;break;  
  > &nbsp;&nbsp;} else {  
  > &nbsp;&nbsp;&nbsp;&nbsp;break labelWhileLoop;  
  > &nbsp;&nbsp;}  
  > }
- continue statement:
  - Stops the current iteration of the loop and immediately starts the next iteration.
  > continue;  
  > continue label;
- for...in statement:
  - A for loop that iterates a specified property within an object.
  > for (apples in appleTree){  
  > &nbsp;&nbsp;code;  
  > }
  - The code would return the references.
  - `"0", "1", "2", "etc."`
- for...of statement:
  - A for loop that iterates over the values of iterable objects.
  > for (apples in appleTree){  
  > &nbsp;&nbsp;code;  
  > }
  - The code would return the values.
  - `"apple", "apple", "apple", "more apples.."`

All of the loops shown will only stop iterating once specified conditions are met (if conditions are set in the first place).

- e.g the for loop above will end once variable i is equivalent to the value of variable someNumber.

If no conditions are set or if the conditions can never be met, then the loops will continue iterating forever.

- e.g:
  > while (1 = 1) {  
  > &nbsp;&nbsp;code;  
  > }  
  - This while loop will go on forever because 1 will always be equal to 1.
