# Class 05

## Culmination

### React POV

React changes the way we look at app building and designing. Component architecture and uni-directional data flow are large deviations from the base JavaScript it comes from.

In React, it is good practice to have components adhere to the single responsibility principle. Components should ideally only have one job. The moment a component grows too large in job scope, we should consider breaking it up into smaller subcomponents.

When building an app, once we have the main component hierarchy and skeleton down, it's often a good idea to start off with a static version. In this static version, the app has almost no user interactivity and is just there to serve as a foundation to build off of. It's easier to build a house first before adding in all the furniture.  
We will ideally want as much hierarchy and prop flow layed out.

Once the static version is built, we then need to add the furniture. State data takes the spot for this analogy. When first starting out on this step, we should aim to add the minimal amount of state data required to create a functional representation of our UI state.  
In order to find the minimal amount of state, we can ask ourselves a few questions:

- What are all the pieces of data that we need in our app.
- Which of these pieces of data are state?
  - Does it remain unchanged over time? If so, it's not state.
  - Is it passed in from a parent via props? If so, it isn't state.
  - Can you compute it based on existing state, or props in your component? If so, it's not state.
  - Everything else is probably state.

Now that we've identified our minimal state data, we need to figure out which components are responsible for each state, whether it be where it changes or where it is owned. It is important to keep in mind that React uses one-way data flow; data passes down from parent to child in the component hierarchy.

We should follow some strategy in order to figure this out:

- Identify components that use state.
- Find their common parent.
- Potentially create a component above the parent if no other spot makes sense.

Once we have all of the state data figure out, we now need to consider adding inverse data flow.

### Higher-Order Functions

Functions that operate on other functions. They either take them as arguments or return them.  
Higher order functions allow us to abstract over actions, instead of simply values. For example, we can have a function that creates new functions.  
Take the example code:

> function greaterThan(n) {
> &nbsp;&nbsp;return m => m > n;
> }
> let greaterThan10 = greaterThan(10);
> console.log(greaterThan10(11));
> // → true

In this function, we return a function that compares any new argument with the argument that was originally passed.

We can see this action abstraction working when it comes to map(). When map is applied to an array, it transforms it by applying a function to all of the elements of the array. We pass an array and a function, an action.

## Things I want to know more about
