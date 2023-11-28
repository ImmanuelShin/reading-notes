# Class 03

## Functions as Props

### Lists and Keys

We can use map() in order to iterate over and transform the contents of an array in a concise manner.  
map() can also be utilized to iterate over and then display the contents of an array in JSX:

- > const numbers = [1, 2, 3, 4, 5];
- > const listItems = numbers.map((number) =>
- > &nbsp; &nbsp; \<li>{number}\</li>
- > );

If you put the above code into a \<ul> element:

- > \<ul>{listItems}\</ul>

It will display an unordered list of number between 1 and 5.

A warning might be displayed when listing out items like this, however. It is because each list item should be provided a specific key.  
We use keys to help React identify what items are changed, added, or removed. Giving elements specific keys gives the elements a stable identity for us and the program to use.  
This might seem like a lot of unique keys eventually, but keys only have to be unique amongst siblings.

[source](https://legacy.reactjs.org/docs/lists-and-keys.html)

### Spread

The spread syntax allows for iterables, such as arrays, to be expanded in places where arguments or elements are expected:

- > const numbers = [1, 2, 3];
- > console.log(sum(...numbers));

Spread lets us use the expanded array in order to use every element. Imagine fanning out a deck of cards to see all 52 of them at once.  
This is useful in many cases:

- Array literals:
  - > const parts = ["shoulders", "knees"];  
  - > const lyrics = ["head", ...parts, "and", "toes"];  
- Copying arrays:
  - > const arr = [1, 2, 3];  
  - > const arr2 = [...arr];
- Array concatenation:
  - > let arr1 = [0, 1, 2];
  - > const arr2 = [3, 4, 5];
  - > // Previously arr1 = arr1.concat(arr2);
  - > arr1 = [...arr1, ...arr2];
- Copying/merging objects:
  - > const obj1 = { foo: "bar", x: 42 };
  - > const obj2 = { bar: "baz", y: 13 };
  - > const mergedObj = { ...obj1, ...obj2 };
- Conditional array values:
  - > const isSummer = false;
  - > const fruits = ["apple", "banana", ...(isSummer ? ["watermelon"] : [])];
  - > // This lets you conditionally add a value to an array without adding an undefined value upon false.

[source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)

### Pass Functions between Components

[Source video](https://www.youtube.com/watch?v=c05OL7XbwXU)

In the video above, the first step the developer does to pass functions was to create the function in the parent component.  
He created increment function which iterates through the people array. If the current iterated object's name matches with the query, the count of that object is increased, and then sent to the ppl variable to update the setState of people.  
Passing the increment function into the child was as simple as just referencing the function into the Person object.  
The child then can use the passed function by using it from its props (this.props.increment());

## Things I want to know more about
