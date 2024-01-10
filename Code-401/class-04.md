# Class 04

## Classes and Objects

Objects encapsulate variables and functions into confined areas. Classes are higher level templates to create new objects. This is useful because we can make very generic classes that might apply to many objects in order to save time, code, and stay organized.

> class MyClass:  
> &nbsp;&nbsp;&nbsp;&nbsp; variable = "blah"  
>  
> &nbsp;&nbsp;&nbsp;&nbsp; def function(self):  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; print("This is a message inside the class.")  
>  
> myobjectx = MyClass()  
> myobjecty = MyClass()  
>  
> myobjecty.variable = "yackity"  
> \# Then print out both values  
> print(myobjectx.variable) &nbsp;&nbsp;&nbsp;&nbsp; \# "blah"  
> print(myobjecty.variable) &nbsp;&nbsp;&nbsp;&nbsp; \# "yackity" 

## Conceptually Recursive

Recursive functions can be difficult to conceputalize, but they all are made up of a common structue of a base case and a recursive case. 

Take the recursive case for calculating n!:

n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1  
n! = n x (n−1)!

We can break this up even futher to explore the base case:

n! = n x (n−1)!   
n! = n x (n−1) x (n−2)!  
n! = n x (n−1) x (n−2) x (n−3)!  
⋅  
⋅  
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3!  
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2!  
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1!  

In python, this translates to:

> def factorial_recursive(n):  
> &nbsp;&nbsp;&nbsp;&nbsp; \# Base case: 1! = 1  
> &nbsp;&nbsp;&nbsp;&nbsp; if n == 1:  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; return 1  
>  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; \# Recursive case: n! = n * (n-1)!  
> &nbsp;&nbsp;&nbsp;&nbsp;else:  
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; return n * factorial_recursive(n-1)  

## pytest

### Fixtures

When writing python tests, rarely are there ever just one or two tests. A large slew of tests are usually going to be created. You can connect tests together using shared data or a network/filesystem.  
Thus, fixtures are very helpful to maintain the resources needed for tests, providing data when needed and releasing data when no longer needed. They also allow tests to be reused and modularized.

## Things I want to know more about
