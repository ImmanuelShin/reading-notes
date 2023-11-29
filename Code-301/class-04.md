# Class 04

## React Forms

### Forms

Forms in React are a little different because form elements naturally keep some internal state. It's often convenient for React forms to have a JavaScript function that handles the submission of the form with access to the data.

Controlled Components is the standard technique to achieve that. In HTML, form elements maintain their own state and update it based on user input while, in React, changeable states are kept in state property components and are updated with setState().  
We combine the two by making the React state the main source of information. This makes it so that the React component that renders the form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a "controlled component".

It seems as though it is better to handle changes upon every keystroke because that is what happens when we put our event handlers onChange in our input fields.

We can target what the user is inputting by adding a name attribute to each element. This is useful when there are multiple controlled input elements being handled.

[source](https://legacy.reactjs.org/docs/forms.html)

### Ternary Operator

Conditional statements will always be necessary in any program. This is why it is important to make them more efficient.

The ternary operator is a concise method of writing conditional statements.

Take this example code:

> if(x===y){  
> &nbsp;&nbsp;console.log(true);  
> } else {  
> &nbsp;&nbsp;console.log(false);  
> }  

Now look at the code written with a ternary operator:

> x===y ? console.log(true) : console.log(false);

Much simpler, a lot smaller.

## Things I want to know more about
