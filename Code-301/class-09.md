# Class 09

## Functional Programming

### Concepts

Functional programming is a method of programming that focuses on trees of expressions rather than state-changing imperative statements.  
This whole paradigm is based around functions, so we should ask ourselves what functions are:

- Pure functions are deterministic: They return the same result if given the same arguments.
- Pure functions are isolated: They don't access any external object and change them except for what they return.

Pure functions have the benefit of being stable, consistent, and predictable. They won't change not matter what else around them change.  

Mutability is the ability for something to change. A thing is immutable if it can't change. Immutable data is needed when we consider Referential transparency.  
Referential transparency is the idea that if we have pure functions that always return the same value if given the same input, and combine those with immutable data, or data that doesn't change, we will know for sure what the result will be; it is referentially transparent.

## Node.js

### Modules and require()

Modules are essentially separate JavaScript files that contain bits of code that can be called whenever. They can be used to simplify or keep short the complexity or length of any single file.  
In order for modules to be used in another file, we need to require it.

> require('./ourModule');

In order to use the functions in our modules, we need to add an additional bit of code to our modules:

> module.exports = someDefinedFunctionInModule;

By exporting the function inside the module, we make it available to other files that required the module.  
Now, since we are now returning the function by exporting it, we need to store it somewhere in our external file.

> const someDefinedFunctionInModule = require('./ourModule');

This now lets us use that function in our other file.

## Things I want to know more about
