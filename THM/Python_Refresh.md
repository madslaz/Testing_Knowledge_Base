## Basic Refresh
### print()
  - print(f) is a function call for formatted string literals, known as f-strings. 
    - Concise way to embed expressions and variables directly into strings
    - Inside the f-string, expressions enclosed in {} are evaluated and values are inserted into strings --> dynamic string creation
    ```
    name = "Maddie"
    print (f"My name is {name}.")
  - To print a string, we have to leverage "". For printing a variable, reference the variable directly: `print(variable)`.
  - pip is Python's package manager
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
## Function
- Functions are blocks of code that can be called at different places within the program.
```
def sayHello(name):
  print("Hello " + name + "! Nice to meet you.")

sayHello("ben")
```
  - def indicates the beginning of a function. Keyword is followed by a name that the programmer defines.
```
def calcCost(item):
  if(item == "sweets"):
    return 3.99 # Decimal is a float
  elif (item == "oranges"):
    return 1.99
  else:
    return 0.99

spent = 10
spent = spent + calcCost("sweets")
print("You have spent:" + str(spent))
``` 
```
def bitcoinToUSD(bitcoin_amount, bitcoin_value_usd):
  bitcoinInUSD = bitcoin_amount * bitcoin_value_usd
  if bitcoinInUSD < 30000:
    print("Broke!")
  return bitcoinInUSD

x = bitcoinToUSD(investment_in_bitcoin, bitcoin_to_usd)
print(x)
```
## Reading and Writing from Files
```
f = open("file_name", "r")
print (f.read())
```
- To open a file, we use the built-in open() function and the "r" parameter standa for read.
- The file variable has a read() method for reading the contents of the file. You can also use the readlines() method to loop over each line in the file; useful if you have a list where each item is on a new line.
```
with open('example.txt', 'r') as file:
  lines = file.readlines()
  for line in lines:
    print(line.strip()) # strip() removes whitespace/newlines
```
```
f = open("demo.txt", "a") # A for append to existing file
f.write("new text!")
f.close() # Close so no more writing can occur
f = open ("demo2.txt, "w") #Create and write
f.write("New file text!")
f.close()
```
- Readlines could be helpful for index-based processing, so for example:
```
with open('students.txt', 'r') as file:
  students = file.readlines()
  print(f"First student: {students[0].strip()}")
  print(f"Last student: {students[-1].strip()}")
  for i in range (len(students)-1):
    print(f"Pair: {students[i].strip()} and {students[i+1].strip()}") # Compare adjacent students
  for i in range(0, len(students), 3):
    print(f"Student #{i}: {students[i].strip()}") # Print every 3rd student
  for i in range (len(students) - 1, -1, -1):
    print(f"Reverse order:{students[i].strip()}")
```
## Indices Reminder
- range(start, end, step)
- The end is not included, so an end of -1 goes up to -1 but does not include it - stops at 0
- If list has 4 items: 1 2 3 4, process as 0 1 2 3, so starting at the end would require len(list) - 1
## Import Libraries
- Import libraries which are a collection of files that contain functions.
```
import datetime
current_time = datetime.datetime.now()
print(current_time)
```
- Call libraries like this: library_name.method_name()
