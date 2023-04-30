### What is the purpose of dunder methods in Python? Provide an example of a commonly used dunder method.

*The purpose :*
<br/>
*we can use it to enrich our classes.*

*Example:*
```
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []

acc = Account('bob')  # default amount = 0
acc = Account('bob', 10)
```
<br/>

### In the video “AI Guru makes $238,800 with misleading paid course,” what was the main ethical issue raised concerning the use of developers’ work, and how might this have been avoided?

<br/>

*The main ethical issue was misleading followers by claiming that the code was his code while it was for others and he just changed the README file, also rarely mentioned the developer's work*

*He can avoid this by honestly crediting the developers and clarifying how much their contributions in his code*

### Describe the Python statistics module and give an example of a function within the module that can be used to perform a common statistical operation.

*Python Statistics Module:*
*The module is not intended to be a competitor to third-party libraries such as NumPy, SciPy, or proprietary full-featured statistics packages aimed at professional statisticians such as Minitab, SAS, and Matlab. It is aimed at the level of graphing and scientific calculators.*

<br/>

```
from statistics import median

data = [20.7, 19.2, 18.3, 14.4]

sorted(data)  
[14.4, 18.3, 19.2, 20.7]

median(data) 
18.75

```


