---
title: "Getting started with python"
datePublished: Mon Dec 18 2023 04:56:09 GMT+0000 (Coordinated Universal Time)
cuid: clqag10pr000008l0b9zi1nfe
slug: getting-started-with-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1702668431702/85ff5367-a4cd-4097-be2b-1baf3db341dc.png
tags: python, python3, python-libraries, python-beginner, python-projects

---

Hey everyone, welcome to the new blog series. Starting today, we will be learning Python. I'll be covering all the major Python topics to get you started. Try to read each one of them and practice on the go. This is the first article of the series, and in this, I'll be sharing some basic things about Python. Without reading this, you can go further, but I felt it is necessary to tell these things because I'm assuming that anyone reading this is a complete beginner, so it could help them.

In each one of these articles, I'll be adding some questions for you to practice.

Now, without further ado, let's start.

## What is Python?

Python is a high-level, object-oriented, interpreted dynamic and multipurpose programming language.

* **Versions:**
    
    1. Python 2.x (October 16, 2000)
        
    2. Python 3.x (December 3, 2000)
        
* **Editor/Interpreter:**
    
    1. Online (Google Colab, Replit, etc.)
        
    2. Offline (IDLE, Jupyter, Spyder, PyCharm, etc.)
        

**Installation:**

* **Windows:** Download and run the installer from [python.org/downloads](http://python.org/downloads). Choose the version and installer that match your system. Alternatively, you can install Python from the Microsoft Store or the Windows Subsystem for Linux.
    
* **Linux:** Use the package manager and command that correspond to your Linux distribution. For example, on Ubuntu and Linux Mint, you can use `sudo apt install python3`. On Fedora, you can use `sudo dnf install python3`. On Arch Linux, you can use `sudo pacman -S python`.
    
* **Mac:** Install Homebrew from [brew.sh](http://brew.sh) and then use `brew install python3` to install Python. Alternatively, you can download and run the installer from [python.org/downloads](http://python.org/downloads) or use other methods.
    

## Working of Python

In the Python programming process, when we have a source code file, such as [`p1.py`](http://p1.py), it undergoes a two-step execution process. First, the source code is translated into a lower-level, platform-independent representation known as bytecode by the Python Virtual Machine (PVM). This bytecode is a set of instructions that the PVM can understand.

After the bytecode is generated, it is then executed by the computer's hardware, producing the final output. This separation of compilation into bytecode and subsequent execution is a key feature of Python's interpreted nature.

<mark>A</mark>\[Source Code (p1.py)\] --&gt;|1. Compilation| <mark>B</mark>\[Bytecode\] B --&gt;|2. Execution| <mark>C</mark>\[Output\]

## To execute Python programs, you can use:

* **Command/interactive mode:** Run Python commands or code one by one in the Python interpreter. Type `python` in your command line or terminal to enter this mode.
    
* **Script mode:** Write Python code in a text file with the `.py` extension and run the whole file as a program. Type `python filename.py` in your command line or terminal to run a Python script.
    

## Keywords in Python

As of now, there are a total of 35 keywords in Python:

| Keyword | Description |
| --- | --- |
| `and` | Logical AND |
| `as` | Alias for module or variable name |
| `assert` | Asserts a condition |
| `break` | Breaks out of a loop |
| `class` | Declares a class |
| `continue` | Skips the rest of a loop |
| `def` | Defines a function |
| `del` | Deletes an object |
| `elif` | Else if condition |
| `else` | Else condition |
| `except` | Catches exceptions |
| `False` | Boolean false value |
| `finally` | Executes code regardless of try-except result |
| `for` | Iterates over a sequence |
| `from` | Import specific attributes or functions from a module |
| `global` | Declares a global variable |
| `if` | Conditional statement |
| `import` | Import a module |
| `in` | Membership test |
| `is` | Object identity test |
| `lambda` | Creates an anonymous function |
| `None` | Represents absence of a value |
| `nonlocal` | Declares a nonlocal variable |
| `not` | Logical NOT |
| `or` | Logical OR |
| `pass` | Placeholder, does nothing |
| `raise` | Raises an exception |
| `return` | Returns a value from a function |
| `True` | Boolean true value |
| `try` | Handles exceptions |
| `while` | Loops while a condition is true |
| `with` | Simplifies resource management using the 'with' statement |
| `yield` | Pauses a generator function and yields a value |

## Data Types

| Data Type | Description | Example |
| --- | --- | --- |
| `int` | Integer | `x = 10` |
| `float` | Floating-point number | `y = 3.14` |
| `str` | String (text) | `name = 'John'` |
| `bool` | Boolean (True or False) | `is_true = True` |
| `list` | List (ordered, mutable sequence) | `numbers = [1, 2, 3]` |
| `tuple` | Tuple (ordered, immutable sequence) | `point = (x, y)` |
| `set` | Set (unordered collection) | `colors = {'red', 'green', 'blue'}` |
| `dict` | Dictionary (key-value pairs) | `person = {'name': 'John', 'age': 30}` |

*<mark>In Python, every value is an object with a type and data. A variable name is a placeholder that points to an object. You can assign any object to any variable name, and the same object to multiple variable names. Changing a variable name does not change the object it points to.</mark>*

For eg:

```python
# Assign an integer object with the value 10 to the variable name x
x = 10

# Print the type and value of x
print(type(x)) # <class 'int'>
print(x) # 10

# Assign a string object with the value "Hello" to the variable name y
y = "Hello"

# Print the type and value of y
print(type(y)) # <class 'str'>
print(y) # Hello

# Assign the same object that x points to to the variable name z
z = x

# Print the type and value of z
print(type(z)) # <class 'int'>
print(z) # 10

# Change the value of x to 20
x = 20

# Print the value of x and z
print(x) # 20
print(z) # 10
```

## Operators in Python

| Operator | Description | Precedence Level | Type |
| --- | --- | --- | --- |
| `**` | Exponentiation | Highest | Arithmetic |
| `+x, -x, ~x` | Urinary positive, negation, bitwise NOT |  | Arithmetic, Bitwise |
| `*, /, //, %` | Multiplication, division |  | Arithmetic |
| `+, -` | Addition, subtraction |  | Arithmetic |
| `<<, >>` | Bitwise shift operators |  | Bitwise |
| `&` | Bitwise AND |  | Bitwise |
| `^` | Bitwise XOR |  | Bitwise |
| \` | \` | Bitwise OR |  |
| `==, !=, <, <=, >, >=` | Comparison operators |  | Relational |
| `not` | Logical NOT |  | Logical |
| `and` | Logical AND |  | Logical |
| `or` | Logical OR |  | Logical |
| `=` | Assignment | Lowest | Assignment |
| `+=, -=, *=, /=, //=, %=` | Compound Assignment |  | Assignment |
| `is, is not` | Identity comparison |  | Identity |
| `in, not in` | Membership test |  | Membership |

## Examples

Now let's take a few examples of how each one of these operators works:

```python
# Arithmetic Operators
result_exponentiation = 2 ** 3  # 2 to the power of 3
result_arithmetic = 10 + 5  # Addition

# Bitwise Operators
bitwise_and = 5 & 3  # Bitwise AND
bitwise_shift_left = 4 << 1  # Bitwise left shift

# Relational Operators
is_equal = 10 == 5  # Equal to
is_not_equal = 10 != 5  # Not equal to

# Logical Operators
logical_not = not True  # Logical NOT
logical_and = True and False  # Logical AND

# Assignment Operators
x = 5  # Assignment
x += 3  # Compound assignment (addition)

# Identity Operators
is_identity = x is 8  # Identity (checks if x is 8)

# Membership Operators
list_example = [1, 2, 3]
is_member = 2 in list_example  # Membership (checks if 2 is in the list)
```

## Now let's practice some questions on the same

### Tell the result of each of the following expression

These are some basic questions for your practice. I will also provide the answers to these questions in the end but before looking at the answers try to solve all the questions yourself.

```python
# Question 1
result1 = 3 ** 2 + 8 // 3 * 2

# Question 2
result2 = (5 + 3) * 2 % 4

# Question 3
x = 5
y = 2
result3 = x // y

# Question 4
result4 = True and not (False or True)

# Question 5
x = 10
x += 5
x //= 3

# Question 6
a = 4
b = 7
result6 = a * 2 + b // 3

# Question 7
result7 = 15 % 4 + 2 ** 3

# Question 8
y = 20
y //= 3
y += 4

# Question 9
result9 = (True or False) and not (False and True)

# Question 10
p = 5
q = 2
result10 = p % q * 3 + p

# Question 11
result11 = not (False or (True and False))

# Question 12
z = 15
z //= 4
z **= 2

# Question 13
m = 8
n = 2
result13 = m / n + m % n

# Question 14
result14 = (False and True) or (True and not False)

# Question 15
r = 10
s = 3
result15 = r % s * 2 - r // s

# Displaying the results
print("Results:")
print("1. ", result1)
print("2. ", result2)
print("3. ", result3)
print("4. ", result4)
print("5. ", x)  # Value of x after Question 5
print("6. ", result6)
print("7. ", result7)
print("8. ", y)  # Value of y after Question 8
print("9. ", result9)
print("10. ", result10)
print("11. ", result11)
print("12. ", z)  # Value of z after Question 12
print("13. ", result13)
print("14. ", result14)
print("15. ", result15)
```

### Solutions

```python
1.  13
3.  2
5.  5
7.  11
9.  True
11. True
13. 4.0
15. -1
```

## Conclusion

In this article, We've covered essential concepts like Python's installation, working process, keywords, data types, and operators. I have also shown some examples and shared some questions. As we are moving forward, remember that practice is key. Take on the challenge of the exercises, and share your solutions in the comments.

*To stay updated on the upcoming articles, make sure to follow me and also don't forget to subscribe to my newsletter.*

*Your commitment to learning Python is commendable, and I'm excited to continue this journey with you. Thank you for being a part. Happy coding!💖*