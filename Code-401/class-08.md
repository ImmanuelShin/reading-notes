# Class 08

## Lists

### List Comprehension Syntax

List comprehension is a method for creating lists.

my_new_list = [ expression for item in iterable_object ]

- The literal iterable_object represents an iterable object such as a list, tuple, set, etc. We use the elements of the iterable_object to create a new list.
- The term item represents an element of the iterable_object.
- The expression represents the operation that we perform on the item. You can perform mathematical operations on item or pass it to a function.
- my_new_list is the list created by executing expression on elements of iterable_object.

List comprehensions can also contain conditionals.

my_new_list = [ expression for item in iterable_object if condition]

Here is an example of using expressions in these list comprehensions:

```
myList=[1,2,3,4,5,6]
print("The original list is:",myList)
newList=[item**2 for item in myList]
print("The output list is:",newList)

The original list is: [1, 2, 3, 4, 5, 6]
The output list is: [1, 4, 9, 16, 25, 36]
```

## Decorators

Decorators wrap functions to modify their behaviors. They are wrappers that are hidden behind syntactic sugar. Python allows decorators to be written in a simpler way using the @ symbol, sometimes called "pie" syntax.

Here is an example of a decorator:

```
def do_twice(func):
  def wrapper_do_twice(*args, **kwargs):
    func(*args, **kwargs)
    return func(*args, **kwargs)
  return wrapper_do_twice
```

We can then decorate a function with it:

```
@do_twice
def greet(name):
    print(f"Hello {name}")

>>> greet("World")
Hello World
Hello World
```

These decorators are powerful in their ability to modify functions in a single line of code. Because they are modular, they are reusable. 

## Things I want to know more about
