### Python preparatory notes

1. Python If-Else
**Task**  
Given an integer, , perform the following conditional actions:

- If  is odd, print `Weird`
- If  is even and in the inclusive range of  to , print `Not Weird`
- If  is even and in the inclusive range of  to , print `Weird`
- If  is even and greater than , print `Not Weird`

**Input Format**

A single line containing a positive integer, .

**Constraints**

**Output Format**

Print `Weird` if the number is weird. Otherwise, print `Not Weird`.

import math

import os

import random

import re

import sys


if __name__ == '__main__':

    n = int(input().strip())

Answer Code:-

if n % 2 == 1:

    print("Weird")

elif n % 2 == 0 and 2 <= n <= 5:

    print("Not Weird")

elif n % 2 == 0 and 6 <= n <= 20:

    print("Weird")

else:

    print("Not Weird")
    

- **Task**  
The provided code stub reads two integers from STDIN,  and . Add code to print three lines where:

1. The first line contains the sum of the two numbers.
2. The second line contains the difference of the two numbers (first - second).
3. The third line contains the product of the two numbers.

**Example**  
  

Print the following:
8
-2
15

**Input Format**

The first line contains the first integer, .  
The second line contains the second integer, .

**Constraints**

  

**Output Format**

Print the three lines as explained above.

**Sample Input 0**

3
2

**Sample Output 0**

5
1
6

**Explanation 0**
3+2=5
3-2=1
3[*]2=6

## Correct Answer

if __name__ == '__main__':

    a = int(input())

    b = int(input())


    # Calculate and print the sum

    print(a + b)

    # Calculate and print the difference (first - second)

    print(a - b)

    # Calculate and print the product

    print(a * b)

  
**Task**  
The provided code stub reads and integer, , from STDIN. For all non-negative integers , print .

**Example**  

The list of non-negative integers that are less than  is . Print the square of each number on a separate line.

0
1
4

**Input Format**

The first and only line contains the integer, .

**Constraints**

**Output Format**

Print  lines, one corresponding to each .

**Sample Input 0**

5

**Sample Output 0**

0
1
4
9
16

## Correct Answer

if __name__ == '__main__':

    n = int(input())

    for i in range(n):

        print(i**2)

## Challenge 

An extra day is added to the calendar almost every four years as February 29, and the day is called a _leap day_. It corrects the calendar for the fact that our planet takes approximately 365.25 days to orbit the sun. A leap year contains a leap day.

In the Gregorian calendar, three conditions are used to identify leap years:

- The year can be evenly divided by 4, is a leap year, unless:
    - The year can be evenly divided by 100, it is NOT a leap year, unless:
        - The year is also evenly divisible by 400. Then it is a leap year.

This means that in the Gregorian calendar, the years 2000 and 2400 are leap years, while 1800, 1900, 2100, 2200, 2300 and 2500 are NOT leap years. [Source](http://www.timeanddate.com/date/leapyear.html)

**Task**

Given a year, determine whether it is a leap year. If it is a leap year, return the Boolean `True`, otherwise return `False`.

Note that the code stub provided reads from STDIN and passes arguments to the `is_leap` function. It is only necessary to complete the `is_leap` function.

**Input Format**

Read , the year to test.

**Constraints**

**Output Format**

The function must return a Boolean value (True/False). Output is handled by the provided code stub.

**Sample Input 0**

1990

**Sample Output 0**

False

**Explanation 0**

1990 is not a multiple of 4 hence it's not a leap year.

## Correct Answer

def is_leap(year):

    leap = False

    # Write your logic here

    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):

        leap = True

    return leap

  

year = int(input())


## Print Function challenge

The included code stub will read an integer, , from STDIN.

Without using any string methods, try to print the following:

Note that "" represents the consecutive values in between.

**Example**  

Print the string .

**Input Format**

The first line contains an integer .

**Constraints**

**Output Format**

Print the list of integers from  through  as a string, without spaces.

**Sample Input 0**

3

**Sample Output 0**

123

## Answer:-

if __name__ == '__main__':

    n = int(input())

    for i in range(1, n + 1):

        print(i, end='')

## Text Alignment Challenge

In Python, a string of text can be aligned _left, right_ and _center_.

**.ljust(width)**

This method returns a left aligned string of length _width_.

```
>>> width = 20
>>> print 'HackerRank'.ljust(width,'-')
HackerRank----------  
```

---

**.center(width)**

This method returns a centered string of length _width_.

```
>>> width = 20
>>> print 'HackerRank'.center(width,'-')
-----HackerRank-----
```

---

**.rjust(width)**

This method returns a right aligned string of length _width_.

```
>>> width = 20
>>> print 'HackerRank'.rjust(width,'-')
----------HackerRank
```

---

**Task**

You are given a partial code that is used for generating the _HackerRank Logo_ of variable _thickness_.  
Your task is to replace the blank (`______`) with _rjust, ljust_ or _center_.

**Input Format**

A single line containing the _thickness_ value for the logo.

**Constraints**

The _thickness_ must be an _odd_ number.  

**Output Format**

Output the desired logo.

**Sample Input**

```
5
```

**Sample Output**

```
    H    
   HHH   
  HHHHH  
 HHHHHHH 
HHHHHHHHH
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHHHHHHHHHHHHHHHHHHHHHH   
  HHHHHHHHHHHHHHHHHHHHHHHHH   
  HHHHHHHHHHHHHHHHHHHHHHHHH   
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
  HHHHH               HHHHH             
                    HHHHHHHHH 
                     HHHHHHH  
                      HHHHH   
                       HHH    
                        H 
```

## Answer

# Enter your code here. Read input from STDIN. Print output to STDOUT

  

def print_hackerrank_logo(thickness):

    c = 'H'

  

    # Top Cone

    for i in range(thickness):

        print((c * i).rjust(thickness - 1) + c + (c * i).ljust(thickness - 1))

  

    # Top Pillars

    for i in range(thickness + 1):

        print((c * thickness).center(thickness * 2) + (c * thickness).center(thickness * 6))

  

    # Middle Belt

    for i in range((thickness + 1) // 2):

        print((c * thickness * 5).center(thickness * 6))

  

    # Bottom Pillars

    for i in range(thickness + 1):

        print((c * thickness).center(thickness * 2) + (c * thickness).center(thickness * 6))

  

    # Bottom Cone

    for i in range(thickness):

        print(((c * (thickness - i - 1)).rjust(thickness) + c + (c * (thickness - i - 1)).ljust(thickness)).rjust(thickness * 6))

  
  

if __name__ == '__main__':

    thickness = int(input())

    print_hackerrank_logo(thickness)



## Text Wrap Challenge

You are given a string  and width .  
Your task is to wrap the string into a paragraph of width .

**Function Description**

Complete the _wrap_ function in the editor below.

_wrap_ has the following parameters:

- _string string:_ a long string
- _int max_width:_ the width to wrap to

**Returns**

- _string:_ a single string with newline characters ('\n') where the breaks should be

**Input Format**

The first line contains a string, .  
The second line contains the width, .

**Constraints**

**Sample Input 0**

ABCDEFGHIJKLIMNOQRSTUVWXYZ
4

**Sample Output 0**

ABCD
EFGH
IJKL
IMNO
QRST
UVWX
YZ

## Answer:

import textwrap

def wrap(string, max_width):

    wrapped_text = textwrap.wrap(string, max_width)

    return '\n'.join(wrapped_text)

  

if __name__ == '__main__':

    string, max_width = input(), int(input())

    result = wrap(string, max_width)

    print(result)

# Designer Door Mat Challenge

Mr. Vincent works in a door mat manufacturing company. One day, he designed a new door mat with the following specifications:

- Mat size must be X. ( is an odd natural number, and  is  times .)
- The design should have 'WELCOME' written in the center.
- The design pattern should only use `|`, `.` and `-` characters.

**Sample Designs**

    Size: 7 x 21 
    ---------.|.---------
    ------.|..|..|.------
    ---.|..|..|..|..|.---
    -------WELCOME-------
    ---.|..|..|..|..|.---
    ------.|..|..|.------
    ---------.|.---------
    
    Size: 11 x 33
    ---------------.|.---------------
    ------------.|..|..|.------------
    ---------.|..|..|..|..|.---------
    ------.|..|..|..|..|..|..|.------
    ---.|..|..|..|..|..|..|..|..|.---
    -------------WELCOME-------------
    ---.|..|..|..|..|..|..|..|..|.---
    ------.|..|..|..|..|..|..|.------
    ---------.|..|..|..|..|.---------
    ------------.|..|..|.------------
    ---------------.|.---------------

**Input Format**

A single line containing the space separated values of  and .

**Constraints**

**Output Format**

Output the design pattern.

**Sample Input**

```
9 27
```

**Sample Output**

```
------------.|.------------
---------.|..|..|.---------
------.|..|..|..|..|.------
---.|..|..|..|..|..|..|.---
----------WELCOME----------
---.|..|..|..|..|..|..|.---
------.|..|..|..|..|.------
---------.|..|..|.---------
------------.|.------------
```

## Challenge Answer:

# Input the values of n and m

n, m = map(int, input().split())

  

# Create the top half of the design

for i in range(1, n, 2):

    pattern = ".|." * i

    print(pattern.center(m, "-"))

  

# Print the welcome message

print("WELCOME".center(m, "-"))

  

# Create the bottom half of the design

for i in range(n-2, 0, -2):

    pattern = ".|." * i

    print(pattern.center(m, "-"))

## String Formatting challenge

Given an integer, , print the following values for each integer  from  to :

1. Decimal
2. Octal
3. Hexadecimal (capitalized)
4. Binary

**Function Description**

Complete the _print_formatted_ function in the editor below.

_print_formatted_ has the following parameters:

- _int number:_ the maximum value to print

**Prints**

The four values must be printed on a single line _in the order specified above_ for each  from  to . Each value should be space-padded to match the width of the _binary_ value of  and the values should be separated by a single space.

**Input Format**

A single integer denoting .

**Constraints**

**Sample Input**

```
17
```

**Sample Output**

    1     1     1     1
    2     2     2    10
    3     3     3    11
    4     4     4   100
    5     5     5   101
    6     6     6   110
    7     7     7   111
    8    10     8  1000
    9    11     9  1001
   10    12     A  1010
   11    13     B  1011
   12    14     C  1100
   13    15     D  1101
   14    16     E  1110
   15    17     F  1111
   16    20    10 10000
   17    21    11 10001

## Challenge Answer:

def print_formatted(number):

    width = len(bin(number)[2:])

    # your code goes here

    for i in range(1, number + 1):

        decimal = str(i).rjust(width)

        octal = oct(i)[2:].rjust(width)

        hexadecimal = hex(i)[2:].upper().rjust(width)

        binary = bin(i)[2:].rjust(width)

  

        print(f"{decimal} {octal} {hexadecimal} {binary}")

  

if __name__ == '__main__':

    n = int(input())

    print_formatted(n)


Closing Time:- [[2023-10-29]] 17:52


