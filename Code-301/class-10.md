# Class 10

## Memory Storage

### JS Call Stack

The JS engine is a single-threaded interpreter comprised of a heap and a single call stack.  
Call stacks are primarily used for function invocations, or calls. Since the stack is singular, the function executions are done one at a time, from top to bottom. This means the stack is synchronous.  
Call stacks are data structures that use Last In, First Out principle. It temporarily stores and manages calls.  
Imagine a tall thin box. You can place something in and take it out immediately. However, the moment you put more than one thing in, you can't take the first thing out right away; you have to take the top most object (the last placed item) out first. Invoked functions, their parameters, and their variables are pushed into the call stack to form a stack frame. The frame is a memory location in the stack and it is cleared when it pops out of the stack.  
The stack can overflow when recursive functions without exit points start filling up the stack. Since the stack has a maximum height, the infinite recursive function invocations will cause the stack to overflow and throw a stack error.

### JavaScript Error Messages

Error messages are an important aspect of coding. Being able to read them will allow a developer to understand what is wrong with what they wrote. Due to the sheer amount of problems that can arise, there are understandably many types of errors:

- Reference error: When a variable is used but is not yet declared.
  - > console.log(foo) // Uncaught ReferenceError: foo is not defined
- Syntax error: When a line of code can't be parsed in terms of syntax.
  - > JSON.parse({ 'foo': 'bar' }) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
- Range error: When an object with a length is given an invalid length.
  - > const arr = [];  
    > arr.length = arr.length - 1; // Uncaught RangeError: Invalid array length
- Type error: When the type of an object/variable is incompatible with the action called upon them.
  - > const foo = {};
    > foo.bar // undefined
    > foo.bar.baz // Uncaught TypeError: Cannot read property of 'baz' of undefined.

On the journey to rid code of an infinite amount of bugs, developers have access to a few useful debugging tools.  
The simplest of these tools being console.log();  
Another tool is the breakpoint. Breakpoints allow you to choose a line of code and see the steps leading up to either the successful or unsuccessful execution of that line. This gives insight into what is breaking and what is working. 
Debugger statements are similar in that, when placed in the code, it will give a history of what has happened before the breakpoint was reached.

## Things I want to know more about

