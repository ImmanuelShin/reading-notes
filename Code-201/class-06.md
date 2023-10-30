# Class 06

## Objects

Objects are collections of related data/functionality. They are made of multiple members, each with names and values. All of these members combine to make a general picture of what our object is.  
Imagine a human "object". They will have:

- A name:  
  - > name: Bob;  
- An age:  
  - > age: 40;  
- Maybe even a catchphrase:
  - > catchphrase() {console.log('Can I fix it? Yes I can!');}

This object is a bunch of information pertaining to the subject, Bob. Through the use of this object, we are now able to send large swaths of information about Bob all bundled into a singular item. Similarly, on the other end, we are also able to handle all of the information about Bob through the convenient usage of arrays, rather than having to take down all his information one at a time.

### Retrieving Information

Some convenient ways to access object information is through the usage of dot notation:

- > person.age;

Or through bracket notation:

- > person["age"];

This is very similar to how you'd access information via arrays, and that's because it is. Objects are sometimes called associative arrays because of how they map strings to values, in the same manner of numbers to values in arrays.  
Generally, dot notation is preferred due to being concise, but sometimes brackets are required:

- Brackets may be required when an object property name is held inside a variable.

### This

"this" is a simple, albeit confusing, keyword that refers to the current object the code is written in.  
Using the more general, "this" over the specific object name allows you to reuse code for multiple different objects.  
Take the following code as an example:  
> const dog = {  
> &nbsp;&nbsp;name: 'Spot',  
> &nbsp;&nbsp;age: 2,  
> &nbsp;&nbsp;color: 'white with black spots',  
> &nbsp;&nbsp;humanAge: function (){  
> &nbsp;&nbsp;&nbsp;&nbsp;console.log(`${this.name} is ${this.age*7} in human years`);  
> &nbsp;&nbsp;}  
> }

"this" refers to the current object, "dog", and it is being used to refer to its own name and age. The main reason to use "this" would be to reuse the console.log() line in the case that you need to define multiple dog objects.

## DOM

Document Object Model: A programming interface for web documents. It interprets the objects that make up web documents and represents them to various programs. The DOM represents the documents as a collection of nodes and objects soo that they can be interacted with and changed by programming languages.  
The DOM is not by itself a programming language. It is merely a medium that JavaScript and other languages use to access web documents. Without it, JavaScript wouldn't have any idea as to what it is looking at. The DOM is essentially a translator.

## Things I want to know more about
