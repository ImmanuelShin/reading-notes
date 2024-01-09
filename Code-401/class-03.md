# Class 03

## Files in Python

Files stores of data and are very important for programmers.  
Files will typically have three main parts:

- Header: metadata about the contents of the file (file name, size, type, and so on).
- Data: contents of the file as written by the creator or editor.
- End of file (EOF): special character that indicates the end of the file.

### File paths

- Folder Path: the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows).
- File Name: the actual name of the file.
- Extension: the end of the file path pre-pended with a period (.) used to indicate the file type.

### Opening Files

> file = open('dog_breeds.txt')

### Closing files

> reader = open('dog_breeds.txt')  
> try:  
> &nbsp;&nbsp; # Further file processing goes here  
> finally:  
> &nbsp;&nbsp; reader.close()  

#### With

> with open('dog_breeds.txt') as reader:
> &nbsp;&nbsp; # Further file processing goes here

The with statement automatically takes care of closing the file once it leaves the with code block. It's much cleaner than the try block and makes handling errors easier.

### Reading

We have a couple of ways to read files:

- .read(): reads the entire file.
- .readline(size=n): reads n characters from the line. If n=0,-1 or empty, reads entire line.
  - Useful when you only want to iterate over one line at a time.
- .readlines(): readsthe remaining lines from the file and returns them as a list.

### Writing

- .write(string): This writes the string to the file.
- .writelines(seq): This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

## Exceptions

Python programs terminate as soon as errors are encountered. 

### Exceptions vs Syntax Error

Syntax errors occur when the parser detects an incorrect statement. Exception errors occur when syntactically correct code results in an error.

Python has various built in exception handlers, but what if we want to have our own exception case?

#### raise

We use raise to throw an exception if a specfic condition occurs.
> x = 10  
> if x > 5:  
> &nbsp;&nbsp; raise Exception('x should not exceed 5. The value of x was: {}'.format(x))

This will raise an error if the value of x exceeds 5.

We can additionally include a try except block to handle exceptions with more grace.

> try:  
> &nbsp;&nbsp; linux_interaction()  
> except:  
> &nbsp;&nbsp; print('Linux function was not executed')

We can include else to try multiple things.

> try:  
> &nbsp;&nbsp; linux_interaction()  
> except:  
> &nbsp;&nbsp; print('Linux function was not executed')  
> else:  
> &nbsp;&nbsp; try:  
> &nbsp;&nbsp;&nbsp;&nbsp; with open('file.log') as file:  
> &nbsp;&nbsp;&nbsp;&nbsp; read_data = file.read()  
> &nbsp;&nbsp; except FileNotFoundError as fnf_error:  
> &nbsp;&nbsp;&nbsp;&nbsp; print(fnf_error)

Finally, we can add a finally to run code regardless of what happens.

> try:  
> &nbsp;&nbsp; linux_interaction()  
> except:  
> &nbsp;&nbsp; print('Linux function was not executed')  
> else:  
> &nbsp;&nbsp; try:  
> &nbsp;&nbsp;&nbsp;&nbsp; with open('file.log') as file:  
> &nbsp;&nbsp;&nbsp;&nbsp; read_data = file.read()  
> &nbsp;&nbsp; except FileNotFoundError as fnf_error:  
> &nbsp;&nbsp;&nbsp;&nbsp; print(fnf_error)  
> finally:  
> &nbsp;&nbsp;&nbsp;&nbsp; print('This is the end of the road')

## Things I want to know more about
