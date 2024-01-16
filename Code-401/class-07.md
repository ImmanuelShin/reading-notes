# Class 07

## Scope

Scope is the concept of how variables and names are looked up inside code. It determines what can see and access what. This concept generally follows the a rule known as LEGB, or Local, Enclosing, Global, and Built-in.

### Understanding Scope

The scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, funcitons, objects, etc.

There are also two general types of scopes:

- Global Scope: Available to the entirety of your code.
- Local Scope: Available to only within the scope.

### LEGB

Python uses the LEGB rule to resolve names:

- **Local (or function) scope** is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. It’s created at function call, not at function definition, so you’ll have as many different local scopes as function calls. This is true even if you call the same function multiple times, or recursively. Each call will result in a new local scope being created.

- **Enclosing (or nonlocal) scope** is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. This scope contains the names that you define in the enclosing function. The names in the enclosing scope are visible from the code of the inner and enclosing functions.

- **Global (or module) scope** is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. Names in this Python scope are visible from everywhere in your code.

- **Built-in scope** is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. Names in this Python scope are also available from everywhere in your code. It’s automatically loaded by Python when you run a program or script.

### Keywords

Python generally follows LEGB, but it also provides the global and nonlocal keywords in order to modify standard behavior.

- global: When you want to assign values to a global name while bypassing the need to make a new local name, you can use the global keyword right in front of the variable name.
- nonlocal: When you want to access nonlocal names from inner functions without having to assign or update them. 

## Big O

Big O is used to measure the resource usage of an algorithm in both time and space. This is important to both analyse how intensive an algorithm is, and to use as benchmarks when trying to improve the overall resource usage.

## Dice

Let's say you want to simulate rolling a die a certain amount of times and calculate the probability of getting a specific number. You can just use random.randint over the interval 1, and 6 in a loop of however many times. From there, we can increase a counter whenver we hit the number we want, and divide that counter by the total number of times we looped.

```
import random
count = 0
def roll():
  return random.randint(1, 6)
for i in range(1, 1001):
  if roll() == 2:
    count += 1
print(count/1000*100)  
```