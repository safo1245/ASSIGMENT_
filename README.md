# PHP & MySQL — Assignment 1
## Jamhuriya University of Science and Technology
---
# Introduction
This assignment contains ten PHP programming exercises designed to practice
basic programming concepts such as conditional statements, loops, operators,
nested loops, divisibility, prime numbers, LCM, HCF, and number manipulation.
Each question was implemented separately in PHP and tested to verify the
expected output.
---
# Question 1 — Greatest and Smallest Number
## Description
The first program compares three integer numbers and finds the greatest and
smallest values.
The program does not use built-in functions such as `max()` or `min()`.
## How It Works
Three numbers are stored in variables. The first number is initially assumed
to be both the greatest and smallest.
The program then compares the other two numbers with these values and updates
the greatest or smallest value when necessary.
## Example
```php
$num1 = 45;
$num2 = 18;
$num3 = 72;

The program compares:

* 45
* 18
* 72

Therefore:

Greatest number: 72
Smallest number: 18

PHP Concepts Used

* Variables
* if statements
* Comparison operators
* Integer values

⸻

Question 2 — Divisible by 3, 5, Both, or Neither

Description

This program checks whether a given number is divisible by 3, 5, both
numbers, or neither.

How It Works

The modulus operator % is used to find the remainder after division.

If the remainder is 0, the number is divisible by that number.

For example:

30 % 3 == 0
30 % 5 == 0

Therefore, 30 is divisible by both 3 and 5.

Output

30 is divisible by both 3 and 5.

PHP Concepts Used

* Modulus operator %
* if
* elseif
* else
* Logical AND operator &&

⸻

Question 3 — Odd Numbers and Even Numbers

Description

This program prints odd numbers from 2 to 20 and even numbers from 35
down to 7.

How It Works

A for loop is used to move through the required range of numbers.

For odd numbers, the program checks:

$i % 2 != 0

For even numbers, it checks:

$i % 2 == 0

A number is odd when it leaves a remainder after division by 2.

A number is even when the remainder is zero.

Output

Odd numbers from 2 to 20:
3 5 7 9 11 13 15 17 19
Even numbers from 35 to 7:
34 32 30 28 26 24 22 20 18 16 14 12 10 8

PHP Concepts Used

* for loop
* Modulus operator %
* Conditional statements

⸻

Question 4 — Numbers Divisible by 2 and 5

Description

This program prints numbers between 2 and 50 that are divisible by both
2 and 5.

How It Works

The program uses a for loop to check every number from 2 to 50.

The following condition checks whether the number can be divided by both
2 and 5 without a remainder:

$i % 2 == 0 && $i % 5 == 0

Output

10 20 30 40 50

These numbers are divisible by both 2 and 5.

PHP Concepts Used

* for loop
* Modulus operator %
* Logical AND operator &&
* if statement

⸻

Question 5 — Reverse a Number

Description

This program reverses the digits of a given number without using the
built-in strrev() function.

For example:

12345 → 54321

How It Works

A while loop is used to process each digit.

The modulus operator obtains the last digit:

$digit = $number % 10;

The digit is then added to the reversed number:

$reverse = ($reverse * 10) + $digit;

Finally, the last digit is removed from the original number:

$number = (int)($number / 10);

This process continues until the original number becomes zero.

Example

Original number: 12345
Reverse number: 54321

PHP Concepts Used

* while loop
* Modulus operator %
* Division
* Variables
* Type casting

⸻

Question 6 — Lowest Common Multiple (LCM)

Description

This program calculates the Lowest Common Multiple (LCM) of two positive
integer numbers.

For example:

LCM of 8 and 12 = 24

How It Works

The program starts checking from the larger of the two numbers.

It continues increasing the value until it finds a number that is divisible
by both input numbers.

The condition used is:

$lcm % $num1 == 0 && $lcm % $num2 == 0

When both conditions are true, the LCM has been found.

Example

For 8 and 12:

24 ÷ 8  = 3
24 ÷ 12 = 2

Therefore:

LCM = 24

PHP Concepts Used

* while loop
* Modulus operator %
* Logical AND &&
* Conditional statements

⸻

Question 7 — Highest Common Factor (HCF)

Description

This program calculates the Highest Common Factor (HCF) of two integer
numbers.

For example:

HCF of 18 and 24 = 6

How It Works

The program checks numbers starting from 1 up to the smaller input number.

For every number, it checks whether both numbers can be divided by it
without a remainder.

The condition is:

$num1 % $i == 0 && $num2 % $i == 0

Whenever a common factor is found, it is stored in the $hcf variable.

The largest common factor becomes the final HCF.

Example

Common factors of 18 and 24 include:

1, 2, 3, 6

The largest one is:

6

Therefore:

HCF = 6

PHP Concepts Used

* for loop
* Modulus operator %
* Logical AND &&
* Variables
* Conditional statements

⸻

Question 8 — Multiplication Table

Description

This program creates a multiplication table from 1 to 12.

The assignment requires the use of nested loops.

How It Works

The outer loop controls the rows:

for ($row = 1; $row <= 12; $row++)

The inner loop controls the columns:

for ($column = 1; $column <= 12; $column++)

The multiplication is performed using:

$row * $column

The result is displayed inside an HTML table.

Example

The table begins with:

1   2   3   4   ... 12
2   4   6   8   ... 24
3   6   9   12  ... 36

and continues until:

12 × 12 = 144

PHP Concepts Used

* Nested for loops
* Multiplication operator
* HTML table
* PHP output

⸻

Question 9 — Prime or Non-Prime Number

Description

This program determines whether a given number is a prime number or
a non-prime number.

How It Works

The program first assumes that the number is prime.

It then checks whether the number can be divided by any number between
2 and the number before it.

If the number can be divided without a remainder, it is not prime.

For example:

17

The number 17 cannot be divided evenly by numbers from 2 to 16.

Therefore:

17 is a prime number.

PHP Concepts Used

* for loop
* if statement
* Modulus operator %
* Boolean variable
* break

⸻

Question 10 — Prime Numbers from 10 to 50

Description

This program finds and displays all prime numbers between 10 and 50.

How It Works

The outer for loop checks every number from 10 to 50.

For each number, another loop checks whether it has any divisor other
than 1 and itself.

If no divisor is found, the number is considered prime.

Output

11 13 17 19 23 29 31 37 41 43 47

These are the prime numbers between 10 and 50.

