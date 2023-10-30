# Class 07

## Object Oriented Programming, HTML Tables

### Domain Modeling

The process of creating conceptual models for certain problems within code. Within are described various entities along with their attributes/behaviors and their constraints.  
Some tips for domain modeling:

-When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.

- Model its attributes with a constructor function that defines and initializes properties.
- Model its behaviors with small methods that focus on doing one job well.
- Create instances using the new keyword followed by a call to a constructor function.
- Store the newly created object in a variable so you can access its properties and methods from outside.
- Use the this variable within methods so you can access the object's properties and methods from inside.

[Source](https://github.com/codefellows/domain_modeling#domain-modeling)

### HTML Tables

Tables are structures made of rows and columns to contain sets of data. These are great for rigid organization, however, they aren't always the best choice.  
HTML tables are for tabular data and tabular data alone. They are not good for entire page layouts. Some issues are:

- Reduced accessibility: Screen readers have a hard time reading tables which makes the output confusing.
- Complexity: Tables involve complex markup structures which makes both writing and maintaining difficult.
- Not automatically responsive: Tables are sized according to their content, so extra styling is needed to make tables look nice across multiple devices.

Some semantic elements for tables:

- \<td>: Table data. These are used to create the smallest container inside a table, a table cell.
- \<tr>: Table row. Used to contain \<td> and make new rows.
- \<th>: Table header. Used to create headers that stand out compared to \<td> cells.

### Constructors

When creating objects, the need to create multiple arises rather quickly. It is a need that object literals cannot satisfy. This is where constructors come in.  
Upon calling a constructor, it:

- Creates a new object.
- Binds "this" to the new object which allows "this" to be used.
- Runs the code within the constructor.
- Returns the new object.

Example constructor:
> function Person(name) {  
> &nbsp;&nbsp;this.name = name;  
> &nbsp;&nbsp;this.introduceSelf = function () {  
> &nbsp;&nbsp;&nbsp;&nbsp;console.log(`Hi! I'm ${this.name}.`);  
> &nbsp;&nbsp;};  
>}

To call this constructor:
> const salva = new Person("Salva");

Using these constructors, we can severely reduce the amount of lines needing to be written by using a clean constructor call.  
Notice how "this" is able to be used even when being called. That's because constructors make it so that "this" is bound into the newly created object.

### Object Prototypes

Prototypes are properties that reference objects. Every JavaScript function has a prototype. What makes prototypes useful is that they allow us to create prototypes rather than needing actual methods. We can create new methods that all instances of the function can now share.  
Imagine a lock maker. Every lock this company makes will require a unique key, but what if we needed a key that could work on them all. We create a signature on every lock, or a prototype method, that will accept a specific master key, or the created method. Now, every lock will able to be opened using this key; every lock inherits this key signature.  
From my limited understanding, that is how prototypes work. They allow for newly created methods to be inherited and shared amongst all repeated objects.

## Things I want to know more about
