# Day 4: Class vs. Instance

**Objective**
In this challenge, we're going to learn about the difference between a _class_ and an _instance_; because this is an _Object Oriented_ concept, it's only enabled in certain languages. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-class-vs-instance/tutorial) tab for learning materials and an instructional video!

**Task**
Write a _Person_ class with an instance variable, _**age**_, and a constructor that takes an integer, _**initialAge**_, as a parameter. The constructor must assign _**initialAge**_ to _**age**_ after confirming the argument passed as _**initialAge**_ is not negative; if a negative argument is passed as _**initialAge**_, the constructor should set _**age**_ to _**0**_ and print `Age is not valid, setting age to 0.`. In addition, you must write the following instance methods:

1. _yearPasses()_ should increase the _**age**_ instance variable by _**1**_.
1. _amIOld()_ should perform the following conditional actions:
    * If _**age < 13**_, print `You are young.`.
    * If _**age >= 13**_ and _**age < 18**_, print `You are a teenager.`.
    * Otherwise, print `You are old.`.

To help you learn by example and complete this challenge, much of the code is provided for you, but you'll be writing everything in the future. The code that creates each instance of your _Person_ class is in the _main_ method. Don't worry if you don't understand it all quite yet!

**Note:** Do not remove or alter the stub code in the editor.

**Input Format**
Input is handled for you by the stub code in the editor.

The first line contains an integer, _**T**_ (the number of test cases), and the _**T**_ subsequent lines each contain an integer denoting the _**age**_ of a Person instance.

**Constraints**

* _**1 <= T <= 4**_
* _**-5 <= age <= 30**_

**Output Format**
Complete the method definitions provided in the editor so they meet the specifications outlined above; the code to test your work is already in the editor. If your methods are implemented correctly, each test case will print _**2**_ or _**3**_ lines (depending on whether or not a valid _**initialAge**_ was passed to the constructor).

**Sample Input**
```
4
-1
10
16
18
```

**Sample Output**
```
Age is not valid, setting age to 0.
You are young.
You are young.

You are young.
You are a teenager.

You are a teenager.
You are old.

You are old.
You are old.
```

**Explanation**
_Test Case 0_: _**initialAge = -1**_
Because _**initialAge < 0**_, our code must set  to  and print the "Age is not valid..." message followed by the young message. Three years pass and _**age = 3**_, so we print the young message again.

_Test Case 1_: _**initialAge = 10**_
Because _**initialAge < 131**_, our code should print that the person is young. Three years pass and _**age = 13**_, so we print that the person is now a teenager.

_Test Case 2_: _**initialAge = 16**_
Because _**13 < = initialAge < 18**_, our code should print that the person is a teenager. Three years pass and _**age = 19**_, so we print that the person is old.

_Test Case 3_: _**initialAge = 18**_
Because _**initialAge >= 18**_, our code should print that the person is old. Three years pass and the person is still old at _**age = 21**_, so we print the old message again.

**The extra line at the end of the output is supposed to be there and is trimmed before being compared against the test case's expected output. If you're failing this challenge, check your logic and review your print statements for spelling errors.**

**CODE**
```Python
class Person:
    def __init__(self,initialAge):
        # Add some more code to run some checks on initialAge
        self.age = 0
        if initialAge > 0:
            self.age = initialAge
        else:
            self.age = 0
            print("Age is not valid, setting age to 0.")
    def amIOld(self):
        # Do some computations in here and print out the correct statement to the console
        if age < 13:
            print("You are young.")
        elif age >= 13 and age < 18:
            print("You are a teenager.")
        else:
            print("You are old.")
    def yearPasses(self):
        # Increment the age of the person in here      
        global age
        age += 1

```
