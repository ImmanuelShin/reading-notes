# Class 03

## Continuing HTML

Lists are great ways to organize items and ideas. In HTML, the way to add lists is through a variety of list elements.

- \<ul>: Unordered list. It typically renders as a bulleted list. It doesn't include an order for the list items meaning it is great for a set of list items that don't need to be ordered. Obviously.
  - You typically use the \<ul> element for grouping non-ordered items and to get that nice looking bullet look.
  - Bullet styles can be changed either through nesting the lists, through CSS list-style-type, or through the type attribute.
  - Types: circle, square, disc, and sometimes triangle.
- \<ol>: Ordered list. As the name suggests, it is an ordered list. It renders usually as a numbered list.
  - Use when list items need to be presented in a specific order.
  - List style can be changed either through the type attribute, or CSS list-style-type.
  - Types: numbers, letters, roman numerals.
    - > \<ol type="i">
      > \<li> list item \</li>  
      > \<li> list item \</li>  
      > \<li> list item \</li>  
      > \</ol>  
    - > \<ol start="4">  
      > \<li> 4th item \</li>  
      > \<li> 5th item \</li>  
      > \<li> 6th item \</li>  
      > \</ol>  

## Continuing CSS

The basis of CSS is that every item is surrounded by a box. This is the Box Model. It's boxes all the way down.  
Understanding how these boxes act and interact with other boxes next to, within, or around will determine how well you can manipulate the webpage's look and layout.  
In the box model, each box is made up of multiple boxes within. Take a single div element. The div box will be divided into the:

- Content box: The main area where the content is displayed. This will be the innermost box.
- Padding box: The box directly surrounding the content box. It will give a layer of "padding" between the inner contents and the border box.
- Border box: The border of the padding box. It represents the outermost bounds of the inner content with padding included.
- Margin box: The actual outside of the box. It surrounds the border to create space outside of border box.

Imagine the box model as a house:  
The border box is the outer walls of the house. All the furniture inside of the house represents the content box zone. The airspace between the furniture and the outer walls represents the padding box. Finally, the property's borders represent the margin box. The property lines keep another property's house to be built touching the main house.

## Continuing JavaScript

### Arrays

Arrays are very useful objects that store values within them. They are very useful when needing a place to put a lot of individual values, or when you need to parse through those values.  
Arrays can also store all sorts of data types: strings, numbers, objects, and even other arrays. Yes, you can have multi-dimensional arrays. Arrays can also store multiple different data types. Take this array for example:
> const people = [['pete', 32, 'librarian', null], ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'], ['bill', null, 'artist', null]];

This people array contains three arrays that all contain different values. In order to view the entire contents of the array, a simple loop can be employed:  
> for (const x of people) {
> &nbsp;&nbsp;console.log(x);
> }

This evaluates to:
> ["pete",32,"librarian",null]  
> ["Smith",40,"accountant","fishing:hiking:rock_climbing"]  
> ["bill",null,"artist",null]

### Operators

Operators are a vital component to any JavaScript file, but they also get rather tedious to keep typing out. JavaScript thus has shorthand operators to help ease the coding process. These are just a few:

- Addition Assignment:
  - > x += 2; --> x = x + 2;
- Subtraction Assignment:
  - > x -= 2; --> x = x - 2;
- Multiplication Assignment:
  - > x *= 2; --> x = x * 2;
- Division Assignment:
  - > x /= 2; --> x = x / 2;
- Logical AND Assignment:
  - > x &&= 2; --> x && (x = 2);

Now, operators are simple, but combining them can be a little complicated. Take the following code:
> let a = 10;  
> let b = 'dog';  
> let c = false;  
>  
> // evaluate this  
> (a + c) + b;  

As confusing as this is, it reduces down to "10dog". It seems when adding a boolean value to a number, the number just eats it. Whereas, if the boolean value were to add a string, the two would combine into one large string.  
In the example above, the boolean value is first added to a number, so the number eats it. Afterwards, the string value gets added to the remaining number.

### Conditionals

Conditionals are important when trying to make decisions based on user input. Take for example prompting a simple yes or no question to the user. In order to account for all answers, yes, no, and other answers, a conditional is needed. In the yes or no question example, a simple if statement would suffice.  
The yes or no question is rather simple. However, one can imagine worlds where different results need to be given based off of a user's ID, or an inputted password, or, to a more complex state, when a user in a game completes optional quest requirements and needs a specific reward.

### Loops

Loops are very useful structures as they allow the programmer to complete a large number of basic repetitive tasks.  
For example, let's say the programmer needs to read a bunch of files and copy their contents. Loops allow for a program to repeatedly loop through text files and copy their contents into either a large array or a separate area entirely.

## Things I want to know more about

I wonder how many complex programs break down into just a series of loops and conditionals.
