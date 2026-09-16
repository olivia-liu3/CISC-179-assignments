# 1. While loop
a. Please write Python code using a while loop to perform the following steps.

Take any non-negative and non-zero integer number and name it n0
if the number is even, evaluate a new n0 as n0 ÷ 2;
Otherwise, if the number is odd, evaluate a new n0 as 3 * n0 + 1;
if n0 is not equal to 1, go to point 2.
Sample input: 16
Expected output:
8
4
2
1
steps = 4
```python
def w():
  n0 = 16
  while (n0 > 1):
    if n0 % 2 == 0:
      n0 = n0 / 2
      print(n0)
    elif n0 % 2 == 1:
      n0 = 3 * n0 + 1
      print(n0)
    elif not n0 == 1:
      n0 = n0 / 2
      print(n0)
```
b. Write code that uses a while loop and runs indefinitely. Modify the same code to resolve the infinite loop issue.
```python
# infinite loop:
n = 10
def w2():
  while (n > 10):
    print(n)
    n = (n - 4) * 2

# definite loop:
n = 10
def w3():
  while (n < 100):
    print(n)
    n = (n - 4) * 2
```
c. Write a program that takes two integers as input and asks the user to choose an arithmetic operation to perform with those numbers. At the end of the program, prompt the user with the question, "Do you want to continue?" If the user selects "Y" or "y," the program should restart; otherwise, it should exit and display the message, "Have a good day."
```python
def c():
  decide = "y"
  while decide == "y" or decide == "Y":
    a = int(input("choose an integer: "))
    b = int(input("choose a second integer: "))
    op = input("choose an arithmetic operation (divide, multiply, add, subtract): ")
    if op == "divide":
      print(a / b)
    elif op == "multiply":
      print(a * b)
    elif op == "add":
      print(a + b)
    else:
      print(a-b)
    decide = input("do you want to continue? input Y or y for yes: ")
    if decide == "Y" or decide == "y":
      continue
    else:
      print("Have a good day!")
      break
```


# 2. For loops
a. Write a code that counts the total number of characters in a text and also counts each character individually. For example, consider the sentence "To be, or not to be, that is the question." The code should determine the total number of letters and how many times each letter appears, including specific counts for the letters 't' and 'o', etc. Ignore the upper and lower cases letters, and any punctuations symbols. Use only for loop, while loop, break and continue statements where necessary.
```python
def make():
  base = input("input text: ")
  text = base.lower()
  text_count = 0
  for char in text:
    if char == " " or char == ",":
      continue
    else:
      text_count = text_count + 1
  print("Total number of alphabets:", text_count)
  alpha = 'q', 'w', 'e', 'r', 't', 'y', 'u', 'i', 'o', 'p', 'a', 's', 'd', 'f', 'g', 'h', 'j', 'k', 'l', 'z', 'x', 'c', 'v', 'b', 'n', 'm'
  for letter in alpha:
    n = 0 # resets n count
    letter_count = n
    letter_name = letter
    for char in text:
      if char == letter:
        n = n + 1
        letter_count = n
      else:
        continue
    print(letter_name, "=", letter_count)
```
  
Sample input: To be, or not to be, that is the question
Expected output:
Total number of alphabets: 30
Total number of distinct alphabets are:
T = 7
o = 4
Note: The expected output above is incomplete. The sum of the total distinct alphabets must equal the total number of alphabets in the given text.

# Challenges
Please describe the challenges you faced during the exercise.
- realized decide == "y" or "Y" means (decide == "y") as one componenet and "Y" as the other. "Y" is truthy so its basically dead code that makes the condition always run. Inside I have to write decide in both components.
- I can embed a loop within a loop. this just means that for that round, python will execute ___. can include more statements besides those dealing with the obeject(s) in the loop. 
- for a in b -> a can be anything, its just a name. b must be a defined variable
- a = "a", "b", "c" is called a tuple while a = ["a", "b", "c"] is a list. the difference is that changes can be made to a list but not a tuple
- if letters are "date"/objects that need to be stored somewhere, there must be quotes around them or else they are undefined variables. 
- if im counting something: I should use a variable in the equation (so that the numbers are not hardcoded) and I can define the starting point before the main program starts. 
- coding takes a lot of time
