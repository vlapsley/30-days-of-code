# Day 7: Arrays

**Objective**
Today, we're learning about the Array data structure. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-arrays/tutorial) tab for learning materials and an instructional video!

**Task**
Given an array, _**A**_, of _**N**_ integers, print _**A**_'s elements in _reverse_ order as a single line of space-separated numbers.

**Input Format**
The first line contains an integer, _**N**_ (the size of our array).
The second line contains _**N**_ space-separated integers describing array _**A**_'s elements.

**Constraints**

* _**1 <= N <= 1000**_
* _**1 <= A~i~ <= 10000**_, where _**A~i~**_ is the _**i^th^**_ integer in the array.

**Output Format**
Print the elements of array _**A**_ in reverse order as a single line of space-separated numbers.

**Sample Input**
```
4
1 4 3 2
```

**Sample Output**
```
2 3 4 1
```

**CODE**
```Python

#!/bin/python3

import sys

n = int(input().strip())
if 1 <= n and n <= 1000:
	arr = [int(arr_temp) for arr_temp in input().strip().split(' ')]
	if max(arr) <= 10000 and max(arr) >= 1:
		rarr = reversed(arr)
		for i in rarr:
			print(i, '', end='')

```
