# Class 06

## Random Module

Random number generation is an important aspect to many specific use-cases. Python's random module provides that function. 

Some common use-cases:

- If you want the computer to pick a random number in a given range, pick a random element from a Python list, pick a random card from a deck, flip a coin, etc, you can use the random module in Python.
- You can also use the random module to create random strings while choosing passwords to make your password database more secure or power a random page feature of your website.
- Random modules provide functions to shuffle container objects like lists. Hence, you can use the random module to shuffle a list.

### Random Functions

The random module has a few functions for random use-cases:

- random(): Provides random numbesr between 0 and 1.
- randint(): Provides random integer.
- choice(): Randomly selects an element from a collection object.
- choices(): Randomly selects two or more elements from a list.
- shuffle(): Shuffles elements in place.
- randrange(): Randomly selects an element from a given range.
  - range(start, stop, step).

## Risk Analysis

Risk is defined as the chances of some unwanted behavior or incident happening. We use risk analysis to better understand the problem areas and plan out the project accordingly.

A few possible risks:

- Use of new hardware.
- Use of new technology.
- Use of new automation tool.
- The sequence of code.
- Availability of test resources for the application.

Some risks aren't as troublesome as others. Some may not even appear. In the extreme cases, a few steps have to be taken care of:

- Conduct Risk Assessment review meeting.
- Use maximum resources to work on high-risk areas.
- Create a Risk Assessment database for future use.
- Identify and notice the risk magnitude indicators: high, medium, low.

In order to actually analyze risks:

- Searching the risk.
- Analyzing the impact of each individual risk.
- Measures for the risk identified.

## Test Coverage

Test coverage is a tool used for finding untested parts of a codebase. It is important to test many potential areas of failure. The issue comes with deciding how many tests to make, what it means to have appropriate coverage, and the potential for low quality tests.  
The ideal would be to:

- Rarely get bugs that escape into production.
- Rarely hesitant to change some code for fear it will cause production bugs.

## Big O

Big O notation is a mathematical representation used to describe the upper bound or worst-case time complexity of an algorithm in terms of its input size. It provides a way to analyze and compare the efficiency of algorithms by expressing their growth rates. For example, O(n) signifies linear time complexity, where the execution time increases proportionally with the input size.  
Consider searching for a specific book on a bookshelf. If each book needs to be checked sequentially until the desired one is found, the time taken scales linearly with the number of books (n), making it an O(n) task.