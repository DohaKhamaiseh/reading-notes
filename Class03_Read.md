### usually we face an expcetions happen while writing codes, so we should consider that in mind, by planning what the next step if any expcetion happen,  by using try, expect and finally blockes

## What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?

*The with statement automatically takes care of closing the file once it leaves the with block, even in cases of error. so it will reduce any unwanted behavior if we didn't close the file*

## Explain the difference between Python's ‘read()’ and ‘readline()’ methods for file objects. Provide examples of when to use each method.

 .read(size=-1): This reads from the file based on the number of size bytes. The entire file is read if no argument is passed or None or -1 is passed.

.readline(size=-1): This reads at the most size number of characters from the line. This continues to the end of the line and then wraps back around. If no argument is passed or None or -1 is passed, then the entire line (or the rest of the line) is read.

Examples:
suppose we have a doha.txt file and this is its content :
doha is a computer engineer
her age is 23 year
she feels tired right now

if we read from doha.txt file by using read() method like this:
```
with open('doha.txt', 'r') as reader:
print(reader.read())
```
then we will get this ouput:
 doha is a computer engineer
her age is 23 year
she feels tired right now

but if we read from the file using readline() like this:
```
with open('doha.txt', 'r') as reader:
print(reader.readline(5))  # 5 represents the number of 
characters(bytes) 
```
then we will get this ouput:
doha

## Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.

*In the try clause, all statements are executed until an exception is encountered.*

*except is used to catch and handle the exception(s) that are encountered in the try clause.*

*finally enables us to execute sections of code that should always run, with or without any previously encountered exceptions.*

```
try:
  print(5/0)
except ZeroDivisionError as error:
    print(error)
finally:
    print('Cleaning up')
```
*the code in try block will give error ZeroDivisionError, so in except block we will print the error which is: integer division or modulo by zero
finally, in finally blochblock we will print 'Cleaning up' regardless any excpetions exceptions happend or not, it will always be executed*