## List Comprehensions

### What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.
</br>

*Basic syntax: [ expression for item in list ]*

*The difference:*  
*list comprehensions are a more compact way of creating lists and more flexible than for loops, also saving time.*

*Example: squares = [x**2 for x in range(10)]*
</br>
</br>

### What is a decorator in Python?
*A decorator is a function that takes another function and extends the behavior of the latter function without explicitly modifying it.*

</br>

### Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.

</br>

* How do they work?
*Decorators work by using the '@' symbol followed by the name of the decorator function above the function or class that needs to be modified. When the function or class is executed, the decorator function is called first, and it returns the modified function or class, which is then used instead.*

* Some common use cases :
  * Adding logging or timing functionality to a function or class
  * Implementing authentication or authorization checks for a 
    function or class
  * Implementing caching or memoization of function calls to 
    improve performance
  * Modifying the behavior of a function or class in some other way
  
  </br>

* Simple decorator function :
```
def my_decorator(func):
    def wrapper():
        print("Something is happening before the function is called.")
        func()
        print("Something is happening after the function is called.")
    return wrapper

@my_decorator
def say_whee():
    print("Whee!")

```
