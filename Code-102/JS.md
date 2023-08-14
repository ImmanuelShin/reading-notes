# Dynamic web pages with JavaScript

## Javascript

A lightweight interpreted programming language. Capabilities include:
> runtime object construction, variable parameter lists, function variables, dynamic script creation (via `eval`), object introspection (via `for...in` and `Object utilities`), and source-code recovery (JavaScript functions store their source text and can be retrieved through `toString()`).

JavaScript has three major parts:

- The language.
- The DOM API:
  - How the language interacts with various parts of a web page.
- The server API.

To add JS to an HTML file, you either embed JS code directly inside the file, or you add a line that includes an external JS file.

### Functions

`alert()` will create a pop-up in the browser.
> `<script language="javascript">`
>
> `alert("Hello World");`
>
> `</script>`

`document.write()` changes the content on the page by adding whatever is within the parenthesis.

> `<script>`
>
> `document.write("<h1>Hello World</h1>");`
>
> `</script>`

`console.log()` allows developers to send messages to the console. This can be useful for testing/debugging.

> `<script>`
>
> `console.log("Hello World");`
>
> `</script>`

`prompt()` creates a pop-up window that prompts the user with a textbox that they can fill in.

> `<script>`
>
> `var name = prompt("Your name:", "");`
>
> `document.write("Hello ", name);`
>
> `</script>`

- Information given by the user through prompts or otherwise is called user "input".

### Variables

A container for a value, such as a number or a string.

To declare, or create, a variable, we use keywords such as `let` or `const`, followed by the name of the variable.
> const example_Variable;

To further initialize, or giving it value, we add an equal sign (=) after the variable name followed by the value.
> const example_Variable = "This is the value of this variable";

The equal sign (=) used isn't an "equal to" operator, but rather an "assignment" operator.

In algebra, the following would not make any sense:
> x = x + 5

However, in JS, because (=) is used to assign instead of signaling equivalence, it makes sense. The case above is assigning the value of "x + 5" to x, rewriting the old value of x with the new value of "x + 5".

