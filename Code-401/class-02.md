# Class 02

## TDD

Test-Driven Development is a code writing strategy in which we create code with idea of creating tests along the way.  
The structure that is widely followed is AAA: Arrange, Act, Assert.

- Arrange: Organize data needed to execute specific pieces of code.
- Act: Executing code to be tested.
- Assert: Checking results to see if expected or not.

TDD follows a cycle:

- 🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the GhostBusters, really).
- ✅ Write the feature and make the test pass! (you can dance after that).
- 🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy).  
[source](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

TDD is about creating the software design first. It is more reliable because it is built off a strong foundation certified by tests.

## if __name__ == '__main__':

Essentially a line to check if the file we are reading is imported or our source file. Using this knowledge, we can now run things depending on whether they are being imported or not.

## Recursion

Recursion is when a function calls itself, either directly or indirectly, to form a self feeding loop. It is extremely code efficient when done well and program breaking wrong.

The algorithmic steps for implementing recursion in a function are as follows:

- Step 1: Define a base case: Identify the simplest case for which the solution is known or trivial. This is the stopping condition for the recursion, as it prevents the function from infinitely calling itself.

- Step 2: - Define a recursive case: Define the problem in terms of smaller sub-problems. Break the problem down into smaller versions of itself, and call the function recursively to solve each subproblem.

- Step 3: - Ensure the recursion terminates: Make sure that the recursive function eventually reaches the base case, and does not enter an infinite loop.

- Step 4: - Combine the solutions: Combine the solutions of the sub-problems to solve the original problem.  
[source](https://www.geeksforgeeks.org/introduction-to-recursion-data-structure-and-algorithm-tutorials/)

## Python Modules and Packages

Modules and Packages facilitate modular programming, or just creating reusable code that is good for simplicity and maintainability. They can be the same, technically, but packages are usually collections of modules. These are used to export large portions of related code from your file to make it look nice, easier to read, and a little more sane.

Modules can be created by creating files containing python code with a .py extension.  
They are imported simply by calling their name. They are used in the same manner.
> import myModule  
> myModule.myVariableInMyModule

Packages are imported in the same manner. This time, however, you can import specific modules from the package.
They are used in the same way afterwards.
> from myPackage import myModule

## Things I want to know more about
