# Day 10: Binary Numbers

**Objective**
Today, we're working with binary numbers. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-binary-numbers/tutorial) tab for learning materials and an instructional video!

**Task**
Given a base-_**10**_ integer, _**n**_, convert it to binary (base-_**2**_). Then find and print the base-_**10**_ integer denoting the maximum number of consecutive _**1**_'s in _**n**_'s binary representation.

**Input Format**
A single integer, _**n**_.

**Constraints**

* _**1 <= n <= 10^6^**_

**Output Format**
Print a single base-_**10**_ integer denoting the maximum number of consecutive _**1**_'s in the binary representation of _**n**_.

**Sample Input 1**
```
5
```

**Sample Output 1**
```
1
```

**Sample Input 2**
```
13
```

**Sample Output 2**
```
2
```

**Explanation**
_Sample Case 1:_
The binary representation of _**5**_ is _**101**_, so the maximum number of consecutive _**1**_'s is _**1**_.

_Sample Case 2:_
The binary representation of _**13**_ is _**1101**_, so the maximum number of consecutive _**1**_'s is _**2**_.

**CODE**
```Python
#!/bin/python3

import sys

def consecutive_ones(n):
	# Convert n to binary
	binary = "{0:b}".format(n)
	longestStreak = []
	currentStreak = 0

	for num in binary:
		if num == '1':
			currentStreak += 1
		else:
			longestStreak.append(currentStreak)
			currentStreak = 0
	longestStreak.append(currentStreak)
	return max(longestStreak)

n = int(input().strip())

print(consecutive_ones(n))

```
