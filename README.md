# 🐍 LeetCode Python Practice Projects (111–115)

## 📌 About This Repository

Welcome to my Python programming practice repository! This repository contains five Python projects created to improve my programming skills, logical thinking, and problem-solving abilities.

These projects cover factorial calculations, prime numbers, palindrome checking, digit sums, and finding the largest number in a list.

Each project demonstrates fundamental Python concepts through simple, practical examples.

## 🎯 Objectives

* Strengthen Python programming fundamentals.
* Practise problem-solving and logical thinking.
* Understand functions, loops, and conditional statements.
* Learn mathematical operations and string manipulation.
* Develop skills in lists and number processing.
* Build a portfolio of Python practice projects.

## 💻 Technologies Used

* **Programming Language:** Python 3
* **Code Editor:** Visual Studio Code
* **Version Control:** Git
* **Repository Hosting:** GitHub

## 📂 Projects Included

| No. | Project Name              | Description                                                  |
| --- | ------------------------- | ------------------------------------------------------------ |
| 111 | Factorial of a Number     | Calculates the factorial of a non-negative integer.          |
| 112 | Prime Number Checker      | Checks whether a number is prime.                            |
| 113 | String Palindrome Checker | Checks whether a string reads the same forward and backward. |
| 114 | Sum of Digits             | Calculates the sum of the digits of an integer.              |
| 115 | Largest Number in a List  | Finds the largest number in a list of integers.              |

---

# 1️⃣ Project 111: Factorial of a Number

## Description

This program calculates the factorial of a given integer.

The factorial of a non-negative integer is the product of all positive integers from 1 to that number.

**Example:**

5! = 5 × 4 × 3 × 2 × 1 = 120

The factorial of 0 is 1.

## Python Code

```python
def factorial(n):
    if n < 0:
        return "Factorial is not defined for negative numbers"

    result = 1

    for i in range(1, n + 1):
        result *= i

    return result


number = int(input("Enter a number: "))
print("Factorial:", factorial(number))
```

## Example Output

```text
Enter a number: 5
Factorial: 120
```

## Concepts Learned

* Python functions
* For loops
* Conditional statements
* Multiplication and arithmetic operations
* Handling negative numbers

## Complexity

* **Time Complexity:** O(n)
* **Auxiliary Space Complexity:** O(1)

---

# 2️⃣ Project 112: Prime Number Checker

## Description

This program checks whether a given integer is a prime number.

A prime number is a whole number greater than 1 that has exactly two positive factors: 1 and itself.

Examples of prime numbers include 2, 3, 5, 7, and 11.

## Python Code

```python
def is_prime(number):
    if number < 2:
        return False

    for i in range(2, int(number ** 0.5) + 1):
        if number % i == 0:
            return False

    return True


number = int(input("Enter a number: "))

if is_prime(number):
    print(number, "is a prime number")
else:
    print(number, "is not a prime number")
```

## Example Output

```text
Enter a number: 7
7 is a prime number
```

## Concepts Learned

* Functions
* For loops
* Conditional statements
* Modulo operator (`%`)
* Prime-number algorithms

## Complexity

* **Time Complexity:** O(√n)
* **Auxiliary Space Complexity:** O(1)

---

# 3️⃣ Project 113: String Palindrome Checker

## Description

This program checks whether a string is a palindrome.

A palindrome reads the same forward and backward.

Examples include `madam`, `level`, and `radar`.

This implementation converts the string to lowercase and removes spaces before checking.

## Python Code

```python
def is_palindrome(text):
    text = text.lower().replace(" ", "")
    return text == text[::-1]


text = input("Enter a string: ")

if is_palindrome(text):
    print("The string is a palindrome")
else:
    print("The string is not a palindrome")
```

## Example Output

```text
Enter a string: madam
The string is a palindrome
```

Another example:

```text
Enter a string: hello
The string is not a palindrome
```

## Concepts Learned

* String manipulation
* Functions
* The `lower()` method
* The `replace()` method
* String slicing (`[::-1]`)
* Conditional statements

## Complexity

* **Time Complexity:** O(n)
* **Auxiliary Space Complexity:** O(n)

---

# 4️⃣ Project 114: Sum of Digits

## Description

This program calculates the sum of all digits in an integer.

For example, the sum of the digits of 1234 is:

1 + 2 + 3 + 4 = 10

The program also supports negative integers by using their absolute value.

## Python Code

```python
def sum_of_digits(number):
    number = abs(number)
    total = 0

    while number > 0:
        digit = number % 10
        total += digit
        number //= 10

    return total


number = int(input("Enter a number: "))
print("Sum of digits:", sum_of_digits(number))
```

## Example Output

```text
Enter a number: 1234
Sum of digits: 10
```

Another example:

```text
Enter a number: -567
Sum of digits: 18
```

## Concepts Learned

* While loops
* Modulo operator (`%`)
* Floor division (`//`)
* Arithmetic operations
* Functions
* Handling negative numbers

## Complexity

* **Time Complexity:** O(d), where d is the number of digits.
* **Auxiliary Space Complexity:** O(1)

---

# 5️⃣ Project 115: Largest Number in a List

## Description

This program finds the largest number in a list of integers.

It starts by assuming that the first element is the largest. It then compares every element with the current largest value and updates it whenever a larger number is found.

The program also handles an empty list.

## Python Code

```python
def find_largest(numbers):
    if not numbers:
        return None

    largest = numbers[0]

    for number in numbers:
        if number > largest:
            largest = number

    return largest


numbers = [12, 45, 7, 89, 23]

result = find_largest(numbers)

if result is None:
    print("The list is empty")
else:
    print("Largest number:", result)
```

## Example Output

```text
Largest number: 89
```

## Concepts Learned

* Python lists
* Functions
* For loops
* Comparison operators
* Conditional statements
* Handling empty lists

## Complexity

* **Time Complexity:** O(n), where n is the number of elements.
* **Auxiliary Space Complexity:** O(1)

---

# ⚙️ How to Run the Projects

## Prerequisites

Install the following tools:

* Python 3
* Visual Studio Code

## Step-by-Step Instructions

1. Download or clone the repository to your computer.
2. Open the project folder in Visual Studio Code.
3. Create a separate Python file for each program.
4. Copy the corresponding code into each file.
5. Save the files.
6. Open the VS Code terminal by selecting **Terminal → New Terminal**.
7. Run the Python file you want to test.

For example, to run Project 111:

```bash
python 111.py
```

To run the remaining projects, use the corresponding filenames:

```bash
python 112.py
python 113.py
python 114.py
python 115.py
```

**Note:** These commands assume that the files are named `111.py`, `112.py`, `113.py`, `114.py`, and `115.py`.

## 📚 Overall Learning Outcomes

By completing these projects, I practised:

* Python syntax and functions.
* Loops and conditional statements.
* String manipulation and slicing.
* Mathematical calculations.
* Lists and element comparisons.
* Time and space complexity analysis.
* Writing reusable and readable code.
* Testing programs with example inputs.

## 🚀 Future Improvements

* Add more Python practice problems.
* Explore recursion and advanced algorithms.
* Learn data structures such as stacks, queues, and linked lists.
* Add automated test cases.
* Improve input validation and error handling.
* Practise more beginner, intermediate, and advanced coding challenges.

## 👩‍💻 Author

**Aishwarya**

Python Programming | Problem Solving | Coding Practice

## 📄 License

This repository is intended for educational purposes and personal programming practice.
