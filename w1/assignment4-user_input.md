# 1. User input
### a. Kilograms to Pounds
Write a program that prompts the user to enter the weight of a person in kilograms and outputs the equivalent weight in pounds.

Note: 1 kilogram = 2.2 pounds.

```python
# This is my code
float(input("Input number of kilogram for conversion into pounds: ")) * 2.2
```
### b. Credit Card Interest
Interest on a credit card's unpaid balance is calculated using the average daily balance. Suppose that netBalance is the balance shown in the bill, payment is the payment made, d1 is the number of days in the billing cycle, and d2 is the number of days payment is made before the billing cycle.

The average daily balance is:

averageDailyBalance = (netBalance × d1 - payment × d2) / d1

If the interest rate per month is, say, 0.0152, then the interest on the unpaid balance is:

interest = averageDailyBalance × 0.0152

Write a program that accepts as input netBalance, payment, d1, d2, and interest rate per month. The program outputs the interest.
```python
# Here is my answer
def interest_calculation():
  netBalance = float(input("What is your netBalance: "))
  payment = float(input("What is the amount in the payment made: "))
  d1 = float(input("How many days in billing cycle: "))
  d2 = float(input("How many days before the billing cycle was the payment made: "))
  interest_rate = float(input("What is your interest rate: "))
  averageDailyBalance = (netBalance * d1 - payment * d2) / d1
  interest = averageDailyBalance * interest_rate
  print("Your interest is", interest)


interest_calculation()
```
### c. Distance Between Two Cars
Two cars A and B leave an intersection at the same time. Car A travels west at an average speed of x miles per hour and car B travels south at an average speed of y miles per hour.

Write a program that prompts the user to enter the average speed of both cars and the elapsed time (in hours and minutes) and outputs the shortest distance between the cars.

``` python
# Write your code here
def shortest_distance():
  x = float(input("What is the average speed of Car A: "))
  y = float(input("What is the average speed of Car B: "))
  time_h = int(input("How many whole hours elapsed: "))
  time_m = int(input("How many minutes from the more recent hour elapsed: "))
  time = time_m / 60 + time_h
  distance = ((x * time) ** 2 + (y * time) ** 2) ** 0.5
  print("The shortest distance between the cars is", distance)


shortest_distance()
```

# 2. Troubleshooting
Please troubleshoot the following issues without using Python, and explain your reasoning.

a. hello = "hello"
b. _var = 100
c. !var_1 = 200
d. print = "print me"
e. False = 0
Write your answer here:

All the above besides "c" set the object on the left hand side of the "=" as the variable for the data, which is on the right hand side. 
"c" is erroneous because "!" is an operator or reserved word in python and cannot be used to name a variable.

# Challenges
Please describe the challenges you faced during the exercise.
- kept forgetting to add colon after function
- learned to call a function
- when writing a function, can leave argument blank. if define argument, only integers can be used as argument when attempting to call function
