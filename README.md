PHP Assignment 1 —⸻

Question 1 — Find the Greatest and Smallest Number

Description

This program compares three numbers and determines which number is the largest and which one is the smallest.

Code

<?php
$num1 = 18;
$num2 = 42;
$num3 = 27;
$largest = $num1;
if ($num2 > $largest) {
    $largest = $num2;
}
if ($num3 > $largest) {
    $largest = $num3;
}
$smallest = $num1;
if ($num2 < $smallest) {
    $smallest = $num2;
}
if ($num3 < $smallest) {
    $smallest = $num3;
}
echo "Largest number: $largest <br>";
echo "Smallest number: $smallest";
?>

Output

Largest number: 42
Smallest number: 18

Explanation

The program initially assumes that $num1 is the largest number. It then compares $num2 and $num3 with the current largest value.

The same method is used to find the smallest number.

⸻

Question 2 — Check Divisibility by 3 and 5

Description

This program checks whether a number can be divided by 3, 5, both, or neither without leaving a remainder.

Code

<?php
$value = 30;
$divisibleBy3 = ($value % 3 == 0);
$divisibleBy5 = ($value % 5 == 0);
if ($divisibleBy3 && $divisibleBy5) {
    echo "$value can be divided by both 3 and 5.";
} elseif ($divisibleBy3) {
    echo "$value can be divided by 3 only.";
} elseif ($divisibleBy5) {
    echo "$value can be divided by 5 only.";
} else {
    echo "$value cannot be divided by 3 or 5.";
}
?>

Output

30 can be divided by both 3 and 5.

Explanation

The % operator is used to find the remainder after division.

For example:

30 % 3 == 0
30 % 5 == 0

Since both results are 0, the number 30 is divisible by both 3 and 5.

The && operator means AND, so both conditions must be true.

⸻

Question 3 — Display Odd and Even Numbers

Part 1 — Odd Numbers from 2 to 20

Code

<?php
echo "Odd numbers: ";
for ($number = 2; $number <= 20; $number++) {
    if ($number % 2 == 1) {
        echo $number . " ";
    }
}
?>

Output

Odd numbers: 3 5 7 9 11 13 15 17 19

Explanation

A for loop checks every number from 2 to 20.

The condition:

$number % 2 == 1

checks whether the remainder is 1. If it is, the number is odd.

⸻

Part 2 — Even Numbers from 35 to 7

Code

<?php
echo "Even numbers: ";
for ($number = 34; $number >= 7; $number -= 2) {
    echo $number . " ";
}
?>

Output

Even numbers: 34 32 30 28 26 24 22 20 18 16 14 12 10 8

Explanation

The loop starts at 34 and decreases by 2 after every iteration.

$number -= 2;

This allows the program to generate even numbers in descending order.

⸻

Question 4 — Numbers Divisible by Both 2 and 5

Description

This program displays numbers between 50 and 2 that are divisible by both 2 and 5.

Code

<?php
echo "Numbers divisible by both 2 and 5:<br>";
for ($x = 50; $x >= 2; $x--) {
    if ($x % 10 == 0) {
        echo $x . " ";
    }
}
?>

Output

Numbers divisible by both 2 and 5:
50 40 30 20 10

Explanation

Numbers that are divisible by both 2 and 5 are multiples of 10.

Therefore, the program checks:

$x % 10 == 0

If the remainder is 0, the number is a multiple of 10 and is therefore divisible by both 2 and 5.

⸻

Question 5 — Reverse a Number

Description

This program reverses the digits of a given number without using the built-in strrev() function.

Code

<?php
$original = 6789;
$reversed = 0;
while ($original != 0) {
    $lastDigit = $original % 10;
    $reversed = $reversed * 10 + $lastDigit;
    $original = intdiv($original, 10);
}
echo "Reversed number: " . $reversed;
?>

Output

Reversed number: 9876

Explanation

The program uses a while loop to process each digit.

First, the last digit is obtained using:

$lastDigit = $original % 10;

For 6789, the digits are extracted in this order:

9 → 8 → 7 → 6

The reversed number is then built step by step:

9 → 98 → 987 → 9876

The function:

intdiv($original, 10)

removes the last digit from the original number.

For example:

6789 → 678 → 67 → 6 → 0

The loop stops when the original number becomes 0.

