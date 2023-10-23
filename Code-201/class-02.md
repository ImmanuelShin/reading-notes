# Basics of HTML, CSS & JS

## Introduction to HTML

HTML is a language that allows one to build up a basic structure of a website. Comprised of elements, HTML uses these elements to group up or divide the page into different sections. These elements can be generic, \<div>, or very specific \<footer>. The specific elements are semantic, which means they have specific roles and uses. It is often better to use semantic elements over non-semantic ones for a multitude of reasons: increased legibility, better organization, keyword matching for search algorithms, etc.

One such element is the h# element. It represents a heading level based on the number provided (1-6). A h1 header is a top level heading whereas a h6 header is the lowest level header.

During the coding process, there may be a time when one must use superscript or subscript. In order to do so, one must simply use the \<sup> and \<sub> elements:
> x\<sup>2\</sup> = x<sup>2</sup>  
> H\<sub>2\</sub>O = H<sub>2</sub>O  

Another useful element is the \<abbr> element. As the name suggests, it allows one to expand an abbreviation to the full term if hovered over:
> The institution that has driven much of the outer space exploration today is \<abbr title="National Aeronautics and Space Administration">NASA\</abbr>.  
> The institution that has driven much of the outer space exploration today is <abbr title="National Aeronautics and Space Administration">NASA</abbr>.

## Intro to CSS

Now CSS, as opposed to HTML's structure, is more focused on design. It allows one to style and organize their website beyond what HTML is capable of.  
In order to add CSS to an HTML file, there are three methods available:

- External Stylesheet: A separate file containing all of the styles. It is linked to the HTML file using the \<link> element.
- Internal StyleSheet: An internal section within the HTML file dedicated to styling the other parts of the file. Internal stylesheets are created using the \<style>\</style> element.
- Inline Styles: Foregoing a centralized area to put styles in, inline styles are put within elements, inline with the element tag. Inline styles are generally avoided due to greater disorganization, reduced efficiency, and harder maintenance.

### Basic CSS Example

Take the following code block:
>h2 {  
>&nbsp;&nbsp;color: black;  
>&nbsp;&nbsp;padding: 5px;  
>}

The h2 represents the selector. It is selecting for all h2 elements within whatever HTML file it is linked to.  
The {} represent the bounds of the CSS Declaration block. All properties and values contained within will be applied to the element selected.  
The "color: black;" and "padding: 5px;" represent the properties and values. Properties are the words that appear before the colon. They are the identifiers that indicate what feature is being changed. The values are what appear after the colon and represent how the property's feature is being changed.

## Intro to JavaScript

JavaScript is the final piece to the HTML website. Where HTML adds structure and CSS adds style, JavaScript adds functionality. JS gives a website the ability to dynamically change its contents, interact with the user, and much more.

JavaScript, being a programming language, accomplishes a lot of this using variables. Variables are named containers that hold data types and can be called upon throughout their scope.  
In JavaScript, variables have different types depending on what data they hold. A variable with a string of text enclosed in quotation marks will be of the String type:

> let thisIsAStringVariable = 'This text surrounded by quotation marks makes this variable a string";  

Variables on their own don't amount to much. This is where operators come. Operators are mathematical symbols that produce results from two values. Let's take two variables, a and b, and assign them values.

> let a = 1;  
> let b = 2;

Now let's take these two variables and operate on them.  
Addition:

> a + b;  
> = 3

Subtraction:

> a - b;  
> = -1

Assignment:

> a = b;  
> a is now assigned the value of 2;

Logic:

> a != b;  
> true (a is not equal to b)

Extended use of JavaScript will create the need for repeatable and reusable blocks of code. These are code snippets that appear often enough that a shortcut would ease the repetitive use. In order to create a function, the function keyword must be typed followed by the function name and an open/closed parenthesis. Afterwards, the function's bounds will be created using open/closed curly braces and the contents will be put within.

> function myFunction() {  
> &nbsp;&nbsp;code;  
> }

In order to use, invoke, the newly created function, simply call it's name followed by the parenthesis and a semicolon:

> myFunction();

Functions can be as simple as just being named short so that they can act as a shortcut to a longer piece of code. Or they can be as complicated being an entire functional block of your code within the bounds of a single word.

### Conditional Logic

When adding functionality to a webpage, oftentimes the need to adapt to different inputs will arise. This is where conditional statements come in to play. These statements act as the decision making in JavaScript in response to different user input.  
One of these conditionals is an if statement. If statements are conditionals that check a specific condition and, if the condition evaluates to true, a following block of code will execute.

> if (condition) {  
> &nbsp;&nbsp;(code that executes if condition is true)  
>}

The if statement can be extended to include other conditions. Else if is added to the end of the statement and acts as another if statement, if the first condition does not evaluate to true.

> if (condition) {  
> &nbsp;&nbsp;(code that executes if condition is true)  
> } else if (condition) {  
> &nbsp;&nbsp;(code that executes if second condition is true)  
> }

This else if can be repeated indefinitely, at the cost of runtime and sanity. Just note that the last else if will simply be an else statement that catches every other condition state.

The way that conditions are determined true or false are often tested by comparison operators:

- === and !==: Test to see if one value is identical or not to another value.
- < and >: Test to see if one value is greater than or less than another value.
- <= and >=: Test to see if one value is less than or equal to, or greater than or equal to, another value.

Logical operators are additional ways to more complexly compare values:

- &&: AND; Requires all expressions tested to result in true.

> (1 == 1 && "Abc" = "Abc") -> true

- ||: OR; Requires just one expression to result in true.

> (1 == 1 || "Abc" = "Acb") -> true

## Things I want to know more about

If pudding is synonymous with dessert for British people, could a chocolate bar be considered pudding?