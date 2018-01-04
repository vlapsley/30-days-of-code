# Day 2: Operators

**Objective**
In this challenge, you'll work with arithmetic operators. Check out the [Tutorial](https://www.hackerrank.com/challenges/30-operators/tutorial) tab for learning materials and an instructional video!

**Task**
Given the *meal price* (base cost of a meal), *tip percent* (the percentage of the *meal price* being added as tip), and *tax percent* (the percentage of the *meal price* being added as tax) for a meal, find and print the meal's *total cost*.

**Note:** Be sure to use precise values for your calculations, or you may end up with an incorrectly rounded result!

**Input Format**
There are *3* lines of numeric input:
The first line has a double, *mealCost* (the cost of the meal before tax and tip).
The second line has an integer, *tipPercent* (the percentage of *mealCost* being added as tip).
The third line has an integer, *taxPercent* (the percentage of *mealCost* being added as tax).

**Output Format**
Print `The total meal cost is totalCost dollars.`, where *totalCost* is the rounded integer result of the entire bill (*mealCost* with added tax and tip).

**Sample Input**
```
12.00
20
8
```

**Sample Output**
```
The total meal cost is 15 dollars.
```

**Explanation**
Given:
*mealCost = 12, tipPercent = 20, taxPercent = 8*

Calculations:
*tip = 12 x 20/100 = 2.4*
*tax = 12 x 8/100 = 0.96*
*totalCost = mealCost + tip + tax = 12 + 2.4 + 0.96 = 15.36*
*round(totalCost) = 15*

We round *totalCost* to the nearest dollar (integer) and then print our result:

`The total meal cost is 15 dollars.`

**CODE**
```Python
def get_total_cost_of_meal():
    # original meal price
    meal_cost = float(input())
    # tip percentage
    tip_percent = int(input())
    # tax percentage
    tax_percent = int(input())

    # Write your calculation code here
    tip = meal_cost * (tip_percent / 100)
    tax = meal_cost * (tax_percent / 100)

    # cast the result of the rounding operation to an int and save it as total_cost
    total_cost = int(round(meal_cost + tip + tax))

    return str(total_cost)

# Print your result
print("The total meal cost is " + get_total_cost_of_meal() + " dollars.")
```
