# Day 5: Loops

**Objective**
In this challenge, we're going to use loops to help us do some simple math. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-loops/tutorial) tab to learn more.

**Task**
Given an integer, _**n**_, print its first _**10**_ multiples. Each multiple _**n**_ x _**i**_ (where _**1 <= i <= 10**_) should be printed on a new line in the form: `n x i = result`.

**Input Format**
A single integer, _**n**_.

**Constraints**

* _**2 <= n <= 20**_

**Output Format**
Print _**10**_ lines of output; each line _**i**_ (where _**1 <= i <= 10**_) contains the _**result**_ of _**n**_ x _**i**_ in the form:
`n x i = result`.

**Sample Input**
```
2
```

**Sample Output**
```
2 x 1 = 2
2 x 2 = 4
2 x 3 = 6
2 x 4 = 8
2 x 5 = 10
2 x 6 = 12
2 x 7 = 14
2 x 8 = 16
2 x 9 = 18
2 x 10 = 20
```

**CODE**
```Python
#!/bin/python3

import sys

n = int(input().strip())

if n > 1 and n <= 20:
    i = 1
    while i <= 10:
        sum = n * i
        print (str(n) + ' x ' + str(i) + ' = ' + str(sum))
        i += 1

```
