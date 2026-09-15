# comparision operators  
for each item in list: left number is the ASCII value, right number is the corresponding character. (commas separate between each item)
32 [space], 33 !, 34 ", 35 #, 36 $, 37 %, 38 &, 39 ', 40 (, 41 ), 42 *, 43 +, 44 ,, 45 -, 46 ., 47 /, 48 0, 49 1, 50 2, 51 3, 52 4, 53 5, 54 6, 55 7, 56 8, 57 9, 58 :, 59 ;, 60 <, 61 =, 62 >, 63 ?, 64 @, 65 A, 66 B, 67 C, 68 D, 69 E, 70 F, 71 G, 72 H, 73 I, 74 J, 75 K, 76 L, 77 M, 78 N, 79 O, 80 P, 81 Q, 82 R, 83 S, 84 T, 85 U, 86 V, 87 W, 88 X, 89 Y, 90 Z, 91 [, 92 \, 93 ], 94 ^, 95 _, 96 `, 97 a, 98 b, 99 c, 100 d, 101 e, 102 f, 103 g, 104 h, 105 i, 106 j, 107 k, 108 l, 109 m, 110 n, 111 o, 112 p, 113 q, 114 r, 115 s, 116 t, 117 u, 118 v, 119 w, 120 x, 121 y, 122 z, 123 {, 124 |, 125 }, 126 ~

# 5. Problem-solving
a. Find the largest three integers just using if statements. Take user inputs and display the result.
```python
def greater():
  a = int(input("input 1st value: "))
  b = int(input("input 2nd value: "))
  c = int(input("input 3rd value: "))
  if a >= b >= c:
    print(a , "is greatest integer")
  elif a >= c >= b:
    print(a, "is greatest integer")
  elif b >= a >= c:
    print(b , "is greatest integer")
  elif b >= c >= a:
    print(b , "is greatest integer")
  else:
    print(c , "is greatest integer")
```


b. Identify multiple methods to determine if a number is even or odd. The user will input an integer, and the output will indicate whether it's "odd" or "even." The code should be organized into sections, with comments separating each part. For example
```python
#######################
# Approach 1
def a1():
  a = int(input("input value: "))
  if a % 2 == 1:
    print("integer is odd")
  else:
    print("integer is even")

#######################
# Approach 2
def a2():
  a = int(input("input value: "))
  if a % 10 == 0 or 2 or 4 or 6 or 8:
    print("integer is even")
  else:
    print("integer is odd")

#######################
# Approach 3
def a3():
  a = int(input("input value: "))
  if a / 2 % 1 == 0.5:
    print("integer is odd")
  else:
    print("integer is even")
#######################
```
c. Implement the grading scheme for the CISC 179 course. The grading scheme as follows:
```python
def grade():
  a = int(input("input grade value: "))
  if a >= 90:
    print("Grade letter is A. Work of geniuenly superior quality")
  elif a >= 80:
    print("Grade letter is B. Passing performance falls approximately in the upper distribution of passing grades.")
  elif a >= 71:
    print("Grade letter is C. Passing performance falls approximately in the center of the distribution of all passing grades.")
  elif a >= 65:
    print("Grade letter is D. Passing performance falls approximately in the lower distribution of passing grades.")
  else:
    print("Grade letter is F. Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways.")
```
Grade	Percent	Description
A	>90	Work of genuinely superior quality.
B	80-89	Passing performance falls approximately in the upper distribution of passing grades.
C	71-79	Passing performance falls approximately in the center of the distribution of all passing grades.
D	65-70	Passing performance falls approximately in the lower distribution of passing grades.
F	<65	Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways.
The user inputs a percentage as an integer, and the output displays the corresponding grade along with a description. The logic uses if, elif, and else statements, with comments to clarify each part.

d. Write a code which takes and, or, not as an user input. Create a truth table by writing your expressions. Display the truth table using print() function. Research how the truth tables for logical operators are structured.
def logic():

```python
  a = input("input one logical operator ('and', 'or', or 'not'): ")
  if a == "and":
    print("x", "y", "x and y", sep="\t")
    print("True", "True", True and True, sep="\t")
    print("True", "False", True and False, sep="\t")
    print("False", "True", False and True, sep="\t")
    print("False", "False", False and False, sep="\t")
  elif a == "or":
    print("x", "y", "x or y", sep="\t")
    print("True", "True", True or True, sep="\t")
    print("True", "False", True or False, sep="\t")
    print("False", "True", False or True, sep="\t")
    print("False", "False", False or False, sep="\t")
  else:
    print("x", "not x", sep="\t")
    print("True", not True, sep="\t")
    print("False", not False, sep="\t")
```

e. To determine whether an integer is even or odd using only a bitwise AND operator. the user will input an integer. Your code should utilize the bitwise AND operator to differentiate between even and odd numbers. Finally, use the print() function to display the result. Avoid using any modulus or remainder operators.

```python
def what():
  inte = int(input("input an integer: "))
  if inte & 1 == True:
    print(inte, "is odd")
  else:
    print(inte, "is even")
```
6. Code revision
Revise the code using nested if, elif, and else statements, and add comments to clarify the logic.

name = input("What's your name? ") # user inputs name. user name saved as name
time = int(input("What time is it? ")) # user inputs time. user time saved as time

if (time < 1200):
    print("Hi ", name, ", good morning!", sep="") # time is before 1200, runs this. 
elif (time < 1800):
    print("Hi ", name, ", good afternoon!", sep="") # time is between 1200 and 1800, runs this. 
elif (time > 1800):
    print("Hi ", name, ", good evening!", sep="") # time is after 1800, runs this. 

print("Good Bye")
7. Output verification
What will be the output of the code provided below without using Python?
```python
def hi():
  x = 1
  y = 1.0
  z = "1"
  if x == y: # will be true and run.
    print("one")
  if y == int(z): # will be true and run
    print("two")
  elif x == y: # will not run because was satisfied in the first condition of if
    print("three")
  else: # will not run because no defined comparision/operation is made with the variables.
    print("four")
```
Please execute the code provided above in Python to confirm your result.

# Challenges
Please describe the challenges you faced during the exercise.

- the difference between "is" and == is that "is" is a literal and has to do with comparing if it is same object in memory (if they have the same address) while == compares the content/data/values 
- learned how binaries work 
- the difference between bitwise and logic operator is that bitwise is a calculation of binaries and logic and evaluating if the statement is true or false.
- when writing condition, don't need to specify that condition must be true because python will only run content under condition if condition is true

