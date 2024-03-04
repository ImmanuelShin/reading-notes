# Class 42

## Dunder 

Dunder methods, short for "double underscore" methods, are special methods in Python that have double underscores at the beginning and end of their names. These methods are also known as "magic methods" or "special methods." They enable you to customize the behavior of your classes, making them behave like built-in types.

One common dunder method is __init__, which is used for initializing an object when it is created. Here's an example:

```python
class MyClass:
    def __init__(self, value):
        self.value = value
```

In this example, the __init__ method is called automatically when an instance of MyClass is created. It allows you to set up the initial state of the object. Dunder methods are invoked by the interpreter, and you can define them in your classes to customize various behaviors.

## Iterator

An iterator in Python is an object that implements two methods: `__iter__()` and `__next__()`. Iterators are used to represent a stream of data and allow you to iterate over elements of a container (like a list, tuple, or a custom class) one at a time without exposing the underlying implementation details.

Here's a breakdown of the key concepts:

1.  **`__iter__()` method:**
    -   This method should return the iterator object itself (usually `self`).
    -   It's called when an iterator object is required, typically at the start of a loop.
2.  **`__next__()` method:**
    -   This method should return the next element from the container.
    -   If there are no more elements, it should raise the `StopIteration` exception.
    -   It keeps track of the current state of iteration.

To create a custom iterator, you need to implement these methods in your class. Here's a simple example of a custom iterator for a range of numbers:

```python
class MyRange:
    def __init__(self, start, end):
        self.current = start
        self.end = end

    def __iter__(self):
        return self

    def __next__(self):
        if self.current >= self.end:
            raise StopIteration
        else:
            result = self.current
            self.current += 1
            return result

my_range = MyRange(1, 5)
my_iterator = iter(my_range)

for num in my_iterator:
    print(num)
```

In this example:

-   The `MyRange` class has `__iter__` and `__next__` methods, making it an iterator.
-   The `__iter__` method returns the iterator object (`self`).
-   The `__next__` method returns the next element in the range and updates the current state of the iterator.

## Generator

A generator is a special type of iterable, similar to a function, but it allows you to iterate over a potentially large set of data without creating the entire set in memory at once. Generators are created using a special kind of function called a generator function, which uses the `yield` keyword.

Here are the key differences between a regular function and a generator function:

1.  Execution Pause and Resume:

    -   Regular functions run until they encounter a `return` statement or the end of the function, after which the function is completed.
    -   Generator functions use `yield` to pause the execution and yield a value to the caller. The state of the generator function is saved, and it can be resumed later.
2.  Memory Usage:

    -   Regular functions may create and return a large data structure, consuming memory for the entire structure.
    -   Generators produce values one at a time on-the-fly, allowing them to work with large datasets without storing the entire dataset in memory.

Here's an example of a generator function:

```python
def countdown(n):
    while n > 0:
        yield n
        n -= 1

for number in countdown(5):
    print(number)
```

In this example:

-   The `countdown` function is a generator function because it contains the `yield` keyword.
-   When the generator is iterated over in the `for` loop, the function starts executing from the beginning until it encounters the `yield` statement.
-   The value is yielded to the caller (`number` in this case), and the state of the function is saved.
-   In the next iteration, the function resumes execution from where it was paused, with the updated state.

## Decorators

Decorators are a powerful and flexible way to modify or extend the behavior of functions or methods. A decorator is a design pattern that allows you to wrap a function with additional functionality in a clean and reusable way. Decorators use the `@decorator` syntax to apply them to functions or methods.

The primary use case of decorators is to add or modify behavior to functions without changing their actual code. This is especially useful for cross-cutting concerns, such as logging, authentication, memoization, or performance monitoring.

To create and apply a custom decorator, you define a function that takes another function as an argument, adds some functionality, and returns a new function. You then use the `@decorator` syntax to apply it to the target function or method.

Here's a simple example of a custom decorator that logs information about function calls:

```python
def log_function_call(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with args: {args}, kwargs: {kwargs}")
        result = func(*args, **kwargs)
        print(f"{func.__name__} returned: {result}")
        return result
    return wrapper

# Applying the decorator using the @ syntax
@log_function_call
def add(a, b):
    return a + b

# Using the decorated function
result = add(3, 5)
```

In this example:

-   The `log_function_call` decorator takes a function (`func`) as an argument and defines a new function (`wrapper`) that logs information before and after calling the original function.
-   The `@log_function_call` syntax is used to apply the decorator to the `add` function.
-   When `add(3, 5)` is called, it actually invokes the `wrapper` function created by the decorator, which, in turn, calls the original `add` function with the provided arguments and logs information.

## Things I want to know more about