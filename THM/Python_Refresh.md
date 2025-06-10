## Basic Refresh
### print()
  - print(f) is a function call for formatted string literals, known as f-strings. 
    - Concise way to embed expressions and variables directly into strings
    - Inside the f-string, expressions enclosed in {} are evaluated and values are inserted into strings --> dynamic string creation
    ```
    name = "Maddie"
    print (f"My name is {name}.")
  - To print a string, we have to leverage "". For printing a variable, reference the variable directly: `print(variable)`. 
### Variables and Data Types
  - Variables allow you to store and update data. You have a variable name and a store data to that name.
    | Data Type| Description|
    | ---| ---|
    | String | Used for combinations of characters (letters or symbols) |
    | Integer | Whole numbers |
    | Float | Number that contains decimal points or for fractions |
    | Boolean | True or false options |
    | List | Series of different data types in a collection 
### Miscellaneous
  - Comments start with # symbol. Full comment block, use """
  - Counts from 0
    
## Mathematical Operators
| Operator | Syntax | Example| 
| --- | --- | ---- | 
| Addition | + | 1+1=2 |
| Subtraction | - | 5-1=4 |
| Multiplication | * | 10*10=100 |
| Division | / | 10/2=5 |
| Modulus | % | 10%2=0 |
| Exponent | ** | 5**2=25 |

## Comparison Operators 
| Operator | Syntax | 
| --- | --- | 
| Greater Than | > |
| Less Than | < | 
| Equal To | == | 
| Not Equal To | != | 
| Greater Than or Equal | >= | 
| Less Than or Equal | <= |

## Boolean Operators
- **AND** if x>= 5 AND x<=100, return TRUE if x is a number between 5 and 100
- **OR** if x ==1 or x==10 returns TRUE if x is 1 or 10
- **NOT** if NOT y returns TRUE if y value is FALSE

```
a = 1
if a == 1 or a > 10:
  print("a is either 1 or above 10")
```

```
name = "bob"
hungry = True
if name == "bob" and hungry == True"
  print("Bob is hungry")
elif name == "bob" and not hungry:
  print("Bob is not hungry")
else:
  print("Not sure who this is or if they are hungry")
```

## If Statements
- Allow programs to make decisions based on a condition.
```
"""
    In this project, you'll create a program that calculates the total
    cost of a customers shopping basket, including shipping.
    - If a customer spends over $100, they get free shipping
    - If a customer spends < $100, the shipping cost is $1.20 per kg of the baskets weight
    Print the customers total basket cost (including shipping) to complete this exercise.
"""

customer_basket_cost = 34
customer_basket_weight = 44

# Write if statement here to calculate the total cost
if customer_basket_cost > 100:
  total_cost=customer_basket_cost
  print(total_cost)
elif customer_basket_cost < 100:
  total_cost=1.20*customer_basket_weight
  total_cost=total_cost+customer_basket_cost
  print(total_cost)
```
## For and While Loops
- For and while loops allow for iteration of the program.
- While: Run loop indefinitely or based on a condition.
- For: Iterate over a sequence, such as a list.
```
i = 1
while i <= 10:
  print(i)
  i = i + 1
```
```
websites = ["facebook.com", "twitter.com", "google.com"]
for site in websites:
  print(site)
```
- Can leverage range for for loops, such as `for i in range (101)`
