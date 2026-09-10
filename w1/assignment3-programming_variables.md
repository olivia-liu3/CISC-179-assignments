# Variable memory usage
```python
var1 = 10

# Check the memory address of var1 by using the following statement
print(hex(id(var1)))

var1 = 100
# Check the memory address of var1 again

# Write your code here
var1 = 10
print(hex(id(var1)))
var1 = 100
print(hex(id(var1)))
```

You should see two distinct addresses for var1. Explain why there are two different addresses and what happened to the first one.

Python does not delete the data (10) from the first var1. The memory cell occupied by 10 continues to be there. When 10 is replaced by 100 for var1, a new memory cell with a new address is used to store the 100. However, from now on, the python interpreter will refer to the new memory cell and address as the one associated with var1.  

```python
var2 = 100
# Write your print statement
print(var2)
print(var1)

# Check the memory address of var2. Did the Python interpreter assign a new memory address or reuse the existing one?
It reused the same one.
# Write your code here
print(hex(id(var2)))
```
# Memory map

```python
str1 = "Hello"
str2 = "World"

# Find out the memory addresses of each character in str1 and str2.
# The following is the example
print(hex(id(str1[0])), hex(id(str1[1])))  # where 0 is the first index and 1 is the second index
# Use the same method as described above to find the addresses of additional characters and complete the table below.
Address in hexadecimal	Char
#	0x7ffb3abb3990
# 0x7ffb3abb3f00
# 0x7ffb3abb4050
# 0x7ffb3abb4050
# 0x7ffb3abb40e0
#	0x7ffb3abb3c60
# 0x7ffb3abb40e0
# 0x7ffb3abb4170
# 0x7ffb3abb4050
# 0x7ffb3abb3ed0
```
# Problem-solving
Let the variable x be dog and the variable y be cat. Write the values returned by the following operations: Try solving without writing in Python.

x + y
"the " + x + " chases the " + y
x * 4
Write your answer here
dogcat
the dog chases the cat
dogdogdogdog

If x = 50. Use an assignment statement to increment the value of x by 1.

```python
# Write your code here
x = 50
x + 1
```
# Troubleshooting
Please troubleshoot the following issue without using Python, and explain your reasoning.

a. hello = "hello" 

b. _var = 100

c. !var_1 = 200

d. print = "print me"

e. False = 0

Write your answer here

All the above besides "c" set the object on the left hand side of the "=" as the variable for the data, which is on the right hand side. 
"c" is erroneous because "!" is an operator or reserved word in python and cannot be used to name a variable.  

# Challenges
Please describe the challenges you faced during the exercise.
- learned that everything in a str is an object and is all saved in one memory address in python and the characters within the str are data saved in the address. When specifying the addresses for each character and index in the str, python creates a new memory address to store the new characters, or reuses addresses if it is a repeated character.
