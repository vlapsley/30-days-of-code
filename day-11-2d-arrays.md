# Day 12: 2D Arrays

**Objective**
Today, we're building on our knowledge of _Arrays_ by adding another dimension. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-2d-arrays/tutorial) tab for learning materials and an instructional video!

**Context**
Given a _**6 x 6**_ _2D Array_, _**A**_:

```
1 1 1 0 0 0
0 1 0 0 0 0
1 1 1 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
0 0 0 0 0 0
```

We define an hourglass in _**A**_ to be a subset of values with indices falling in this pattern in _**A**_'s graphical representation:

```
a b c
  d
e f g
```

There are _**16**_ hourglasses in _**A**_, and an _hourglass sum_ is the sum of an hourglass' values.

**Task**
Calculate the hourglass sum for every hourglass in _**A**_, then print the _maximum_ hourglass sum.

**Input Format**
There are _**6**_ lines of input, where each line contains _**6**_ space-separated integers describing _2D Array_ _**A**_; every value in _**A**_ will be in the inclusive range of _**-9**_ to _**9**_.

**Constraints**

* _**-9 <= A[i][j] <= 9**_
* _**0 <= i,j <= 5**_

**Output Format**
Print the largest (maximum) hourglass sum found in _**A**_.

**Sample Input**
```
1 1 1 0 0 0
0 1 0 0 0 0
1 1 1 0 0 0
0 0 2 4 4 0
0 0 0 2 0 0
0 0 1 2 4 0
```

**Sample Output**
```
19
```

**Explanation**
_**A**_ contains the following hourglasses:

```
1 1 1   1 1 0   1 0 0   0 0 0
  1       0       0       0
1 1 1   1 1 0   1 0 0   0 0 0

0 1 0   1 0 0   0 0 0   0 0 0
  1       1       0       0
0 0 2   0 2 4   2 4 4   4 4 0

1 1 1   1 1 0   1 0 0   0 0 0
  0       2       4       4
0 0 0   0 0 2   0 2 0   2 0 0

0 0 2   0 2 4   2 4 4   4 4 0
  0       0       2       0
0 0 1   0 1 2   1 2 4   2 4 0
```

The hourglass with the maximum sum (_**19**_) is:

```
2 4 4
  2
1 2 4
```

**CODE**
```Python
#!/bin/python3

import sys


arr = []
for arr_i in range(6):
	arr_t = [int(arr_temp) for arr_temp in input().strip().split(' ')]
	arr.append(arr_t)

hourglass = [(0, 0), (0, 1), (0, 2), (1, 1), (2, 0), (2, 1), (2, 2)]

print(max(sum(arr[i+x][j+y] for x, y in hourglass) for i in range(4) for j in range(4)))

```
