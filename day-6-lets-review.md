# Day 6: Let's Review

**Objective**
Today we're expanding our knowledge of Strings and combining it with what we've already learned about loops. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-review-loop/tutorial) tab for learning materials and an instructional video!

**Task**
Given a string, _**S**_, of length _**N**_ that is indexed from _**0**_ to _**N - 1**_, print its _even-indexed_ and _odd-indexed_ characters as _**2**_ space-separated strings on a single line (see the _Sample_ below for more detail).

**Note:** _**0**_ is considered to be an even index.

**Input Format**
The first line contains an integer, _**T**_ (the number of test cases).
Each line _**i**_ of the _**T**_ subsequent lines contain a String, _**S**_.

**Constraints**

* _**1 <= T <= 10**_
* _**2 <= length of S <= 10000**_

**Output Format**
For each String _**S~j~**_ (where _**0 <= j <= T - 1**_), print _**S~j~**_'s _even-indexed_ characters, followed by a space, followed by _**S~j~**_'s _odd-indexed_ characters.

**Sample Input**
```
2
Hacker
Rank
```

**Sample Output**
```
Hce akr
Rn ak
```

**Explanation**
Test Case 0: _**S = "Hacker"**_
_**S[0] = "H"**_
_**S[1] = "a"**_
_**S[2] = "c"**_
_**S[3] = "k"**_
_**S[4] = "e"**_
_**S[5] = "r"**_
The _even_ indices are _**0**_, _**2**_, and _**4**_, and the _odd_ indices are _**1**_, _**3**_, and _**5**_. We then print a _single line_ of _**2**_ space-separated strings; the first string contains the ordered characters from _**S**_'s _even_ indices (**Hce**), and the second string contains the ordered characters from _**S**_'s _odd_ indices (**akr**).

Test Case 1: _**S = "Rank"**_
_**S[0] = "R"**_
_**S[1] = "a"**_
_**S[2] = "n"**_
_**S[3] = "k"**_
The _even_ indices are _**0**_ and _**2**_, and the _odd_ indices are _**1**_ and _**3**_. We then print a _single line_ of _**2**_ space-separated strings; the first string contains the ordered characters from _**S**_'s _even_ indices (**Rn**), and the second string contains the ordered characters from _**S**_'s _odd_ indices (**ak**).

**CODE**
```Python

T = int(input())

if 1 <= T and T <= 10:
    for i in range(T):
        S = input()
        if 2 <= len(S) and len(S) <= 10000:
            print(S[::2], S[1::2])
        else:
            print('Error.')
else:
    print('Error.')

```
