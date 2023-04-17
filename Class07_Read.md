## Python Scope
### Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.

*The scope of a name defines the area of a program in which we can unambiguously access that name, such as variables, functions, objects, and so on. A name will only be visible to and accessible by the code in its scope.*

#### Local Scope vs. Global Scope :
 ```
var_global = 100 # this is a global variable 
def fun():
    var_local = 10 # this is a local variable because it is inside local scope
    print(var_global) # we can access the global variable anywhere in code
    return var_local

print(fun()) 
100
10

#this is acceptable beacuse var_global is an global variable 
print(var_global) 
100
# This is not acceptable because var_local can't be seen outside the fun scope 
# It is a local variable, we can access it just inside the fun scope
print(var_local) 
NameError: name 'var_local' is not defined

 ```

 ### How do the global and nonlocal keywords work in Python, and in what situations might you use them?

**global:** any global keyword that is followed by a name will be mapped to the global or module scope in which we define it.
we might use it if we need to modify the  global variable inside the local or nonlocal scope

**nonlocal:** any nonlocal keyword that is followed by a name will be mapped to the nonlocal/enclosing scope in which we define it. we might use it if we need to modify the nonlocal /enclosing variable(outter) inside the local  scope(inner)

##  Big O notation
### In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.

*Big O notation is an essential tool for algorithm analysis, as it allows us to compare the efficiency and scalability of different algorithms and choose the best one for a particular task because its purpose is: to provide a way to compare the efficiency of different algorithms. By analyzing the Big O notation of an algorithm, we can get an idea of how much time and resources it will take to execute the algorithm for a given input size. This can help us choose the best algorithm for a particular task.*

## Rolling Dice
### Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.

```
import random

def roll_dice():
    return random.randint(1, 6)


result = roll_dice() #now result has a random integer value between 1 and 6 and each time we call the roll_dice the result maybe different 
print("The result of the dice roll is:", result)

num_trials = 1000
num_sixes = 0

for i in range(num_trials): # to check the occurrence of 6 in each trial 
    result = roll_dice()
    if result == 6:
        num_sixes += 1 # to count the occurrence of 6

probability = num_sixes / num_trials # the probability of 6 is how much 6 appear from all trails
print("The probability of rolling a 6 is:", probability)

```

## Things I want to know more about