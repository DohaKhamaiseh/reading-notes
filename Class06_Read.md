## How to Use the Random Module 
### The random module has a lot of functions such as :
1. randint(first, last): used to generate an integer number between the range of first and end 

2. random(): used to generate a  floating point number between the range of 0 and 1, it can be used for any range bigger than 1 by multiplying the function with that number

3. choice(list): is used to select a random element from a collection object like a list, set, tuple, etc. 

4. shuffle(list): used to shuffle randomly the order of a given list or any collection object

5. randrange():  used to select a random element from a given range. It takes three numbers namely start, stop, and step as input argument. After execution, it generates a randomly selected element from the range(start, stop, step).

### Answer  :
**firstly to use any function from the random module we should import the random like this:  import random
then to generate random numbers we can use either random() function which will produce floating point numbers between 0 and 1 or use randint(start, end) function to produce integer numbers between the start and the end arguments. 
to make selections from a list we  can use choice(list) function 
for some most common functions available within the module, already mentioned  three of them, the remaining are : 
shuffle(list)  which will shuffle the order of any list
 randrange(start, stop, step) which will select a random element between the start and the end and increase the start-by-step argument** 

## What is Risk Analysis?
### Risk analysis is identifying the risks in applications or software we built and prioritizing them to test.

### we use risk analysis at the beginning of a project to highlight the potential problem areas then after knowing about the risk areas the risk analysis helps us as developers to mitigate the risks.

### The risk could be from any of these categories:
1. Business Risks    
2. Testing Risks
3. Premature Release Risk 
4.  Software Risks

### we can perform risk analysis by following these steps :
1. Searching the risk
2. Analyzing the impact of each individual risk
3. Measures for the risk identified
   

### Answer : 
**In the context of software development, what is risk analysis?
written above**

**what are the key steps involved in conducting a risk analysis for a software project?**

 **1.identifying the risks in applications or software that you built.**

 **2.prioritizing them to test..**

 **3.The process of assigning the level of risk is done.**

 **4.The categorization of the risks takes place hence, the impact of the risk is calculated.**
   
## Test Coverage
###  the value of coverage analysis is that it helps us to find which bits of our code isn't being tested. but, 
>If a part of your test suite is weak in a way that coverage can detect, it's likely also weak in a way coverage can't detect.

### Answer : 
**What is test coverage and why is it an important (or potentially misleading) metric in software testing?**

**written above**

## Big O :

### WHAT
 *is a way used to describe the Worst Case of efficiency an algorithm can have in performing its job.*

### HOW 
*analyzing the algorithm and determining the number of operations it performs as the input size grows. We then express this as a function of the input size and simplify the function by ignoring lower-order terms and constants.*

### EXAMPLE:
 *An example of an everyday task that demonstrates O(n) time complexity is counting the number of items in a grocery bag. The time it takes to count the number of items in the bag increases linearly with the number of items. For example, if there are 10 items in the bag, it will take roughly twice as long to count the items compared to a bag with 5 items. Similarly, if there are 20 items in the bag, it will take roughly twice as long as a bag with 10 items. This demonstrates O(n) time complexity, where n is the number of items in the bag.*

## Things I want to know more about
