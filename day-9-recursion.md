# Day 9: Recursion

**Objective**
Today, we're learning and practicing an algorithmic concept called _Recursion_. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-recursion/tutorial) tab for learning materials and an instructional video!

**Recursive Method for Calculating Factorial**
```
function factorial is:
input: integer N such that N >= 0
output: [N × (N-1) × (N-2) × … × 1]

	1. if N is 0, return 1
	2. otherwise, return [ N × factorial(N-1) ]

end factorial
```

**Task**
Write a _factorial_ function that takes a positive integer, _**N**_ as a parameter and prints the result of _**N!**_ (_**N**_ factorial).

**Note**: If you fail to use recursion or fail to name your recursive function _factorial_ or _Factorial_, you will get a score of _**0**_.

**Input Format**
A single integer, _**N**_ (the argument to pass to _factorial_).

**Constraints**

* _**2 <= N <= 12**_
* Your submission must contain a recursive function named _factorial_.

**Output Format**
Print a single integer denoting _**N!**_.

**Sample Input**
```
3
```

**Sample Output**
```
6
```

**Explanation**
Consider the following steps:

1. _**factorial(3) = 3 x factorial(2)**_
1. _**factorial(2) = 2 x factorial(1)**_
1. _**factorial(1) = 1**_

From steps _**2**_ and _**3**_, we can say _**factorial(2) = 2 x 1 = 2**_; then when we apply the value from _**factorial(2)**_ to step _**1**_, we get _**factorial(3) = 3 x 2 x 1 = 6**_. Thus, we print _**6**_ as our answer.

**CODE**
```Python
#!/bin/python3

import sys

def factorial(n):
	# Complete this function
	if n <= 1:
		return 1
	else:
		return n * factorial(n - 1)

if __name__ == "__main__":
	n = int(input().strip())
	result = factorial(n)
	print(result)

```
