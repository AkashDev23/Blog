---
title: "Functions in Python"
datePublished: Fri Dec 22 2023 05:48:12 GMT+0000 (Coordinated Universal Time)
cuid: clqg7nckk000808l64lphhf4n
slug: functions-in-python
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1702914225432/0cdb9631-4d9c-4879-83e9-15f474795ee0.jpeg
tags: python, python3, python-libraries, python-beginner, python-projects

---

This is the third article of the series. If you haven't read the previous two articles yet, I recommend you to go and read them first to have a better understanding of this one. Make sure to read till the end as I have added a few questions for you guys to check your understanding. With that said, let's start.

In Python, a function is a block of organized, reusable code, i.e. used to perform a single task or related actions. Functions provide better modularity of your application and a high degree of code reusing.

There are two kinds of functions available:

1. Built-In Functions
    
2. User-defined Functions
    

## Built-in functions

Built-in functions are the predefined functions available in the Python package. Python comes with a variety of built-in functions that provide useful functionality. Here are some commonly used built-in functions along with examples:

### 1\. `len()`

Returns the length (the number of items) of an object.

```python
string_length = len("Hello, World!")
print("Length of the string:", string_length)
# Length of the string: 13
```

### 2\. `print()`

Prints the specified message to the console.

```python
print("Hello, Python!")
# Hello, Python!
```

### 3\. `type()`

Returns the type of an object.

```python
data_type = type(42)
print("Type of the variable:", data_type)
# Type of the variable: <class 'int'>
```

### 4\. `int()`, `float()`, `str()`

Converts a value to an integer, float, or string, respectively.

```python
num_str = "42"
num_int = int(num_str)
num_float = float(num_str)

print("Integer:", num_int)
print("Float:", num_float)
# Integer: 42
# Float: 42.0
```

### 5\. `input()`

Reads a line from the console.

```python
user_input = input("Enter your name: ")
print("Hello, " + user_input + "!")
# Enter your name: Akash
# Hello, Akash!
```

### 6\. `range()`

Generates a sequence of numbers within a specified range.

```python
numbers = list(range(1, 6))
print("Generated range of numbers:", numbers)
# Generated range of numbers: [1, 2, 3, 4, 5]
```

### 7\. `sum()`

Returns the sum of all elements in an iterable.

```python
numbers = [1, 2, 3, 4, 5]
total = sum(numbers)
print("Sum of numbers:", total)
# Sum of numbers: 15
```

### 8\. `max()` and `min()`

Returns the maximum or minimum value in an iterable or among two or more arguments.

```python
max_value = max(10, 20, 30)
min_value = min([5, 8, 2, 10])

print("Max value:", max_value)
print("Min value:", min_value)
# Max value: 30
# Min value: 2
```

### 9\. `abs()`

Returns the absolute value of a number.

```python
absolute_value = abs(-10)
print("Absolute value:", absolute_value)
# Absolute value: 10
```

### 10\. `sorted()`

Returns a new sorted list from the elements of any iterable.

```python
unsorted_list = [3, 1, 4, 1, 5, 9, 2]
sorted_list = sorted(unsorted_list)

print("Original list:", unsorted_list)
print("Sorted list:", sorted_list)
# Original list: [3, 1, 4, 1, 5, 9, 2]
# Sorted list: [1, 1, 2, 3, 4, 5, 9]
```

These are just a few examples of the many built-in functions Python provides.

## User-defined functions

### Defining a Function:

You can define a function using the `def` keyword, followed by the function name, parameters (if any), a colon, and an indented block of code.

```python
def greet(name):
    """This function greets the person passed in as a parameter."""
    print(f"Hello, {name}!")

# Call the function
greet("Akash")
```

### Function Parameters Or Arguments:

Functions can take parameters, which are values you can pass to the function. These parameters are specified in the parentheses following the function name. Depending on the number of arguments and return values, a function can be defined in 4 ways:

1. Function with no argument & no return value.
    
2. Function with arguments but no return value.
    
3. Function with no arguments but return value.
    
4. Function with arguments and with the return value.
    

```python
def add_numbers(a, b):
    """This function adds two numbers and returns the result."""
    result = a + b
    return result

sum_result = add_numbers(3, 5)
print("Sum:", sum_result)
```

### Return Statement:

A function can return a value using the `return` statement. If no `return` statement is present, the function returns `None` by default.

> A function that returns a value is called a fruitful function, whereas a function without any return value is called a void function.

```python
def multiply(a, b):
    """This function multiplies two numbers and returns the result."""
    return a * b

product = multiply(4, 6)
print("Product:", product)
```

### Variable Scope:

Variables defined inside a function have local scope, meaning they are only accessible within that function. Variables defined outside a function have global scope.

```python
global_variable = "I'm global"

def local_scope_example():
    local_variable = "I'm local"
    print(local_variable)
    print(global_variable)  # Accessing global variable inside the function

local_scope_example()
# print(local_variable)  # This would result in an error since local_variable is not accessible here
```

## Types of Arguments:

In Python, function arguments can be categorized into four types: required (positional), keyword, default, and variable-length arguments. Let's discuss each type:

### 1\. Required (Positional) Arguments:

These are the most basic type of arguments. They are passed to a function in the order they are defined in the function signature. The number of arguments passed must match the number of parameters in the function.

Example:

```python
def add_numbers(a, b):
    return a + b

result = add_numbers(3, 5)
print("Sum:", result)
```

### 2\. Keyword Arguments:

Keyword arguments are identified by the parameter names, and the values are passed with the parameter names. This allows you to pass values in any order and explicitly specify which parameter each value corresponds to.

Example:

```python
def greet(name, message):
    print(f"Hello, {name}! {message}")

greet(message="How are you?", name="Akash")
```

### 3\. Default Arguments:

Default arguments have a default value specified in the function signature. If a value is not provided for the parameter when the function is called, the default value is used.

Example:

```python
def power(base, exponent=2):
    return base ** exponent

result1 = power(2)       # 2^2 (default exponent)
result2 = power(2, 3)    # 2^3

print("Result 1:", result1)
print("Result 2:", result2)
```

### 4\. Variable-Length Arguments:

Python allows you to define functions that can accept a variable number of arguments. There are two types of variable-length arguments: `*args` (arbitrary positional arguments) and `**kwargs` (arbitrary keyword arguments).

#### a. Arbitrary Positional Arguments (`*args`):

These allow a function to accept any number of positional arguments. The arguments are passed as a tuple.

Example:

```python
def add(*args):
    result = 0
    for num in args:
        result += num
    return result

sum_result = add(1, 2, 3, 4, 5)
print("Sum:", sum_result)
```

#### b. Arbitrary Keyword Arguments (`**kwargs`):

These allow a function to accept any number of keyword arguments. The arguments are passed as a dictionary.

Example:

```python
def display_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

display_info(name="Akash", age=21, country="India")
```

These four types of arguments provide flexibility and allow you to create functions that can handle various input scenarios.

## \_\_name\_\_ variable

The `__name__` variable is a special built-in variable in Python that is used to determine if a Python script is being run as the main program or if it is being imported as a module into another script. When a Python script is executed, the `__name__` variable is set to `"__main__"` if the script is the main program being run. If the script is imported as a module into another script, the `__name__` variable is set to the name of the script (i.e., the module name).

Here's a common use case to illustrate the concept:

```python
# my_module.py

def some_function():
    print("Function in my_module")

if __name__ == "__main__":
    print("This is the main program.")
    some_function()
```

In this example, when `my_`[`module.py`](http://module.py) is run as the main program, the `__name__` variable is set to `"__main__"`, and the code block under `if __name__ == "__main__":` is executed. If `my_`[`module.py`](http://module.py) is imported as a module into another script, the `__name__` variable is set to `"my_module"`, and the code block under `if __name__ == "__main__":` is skipped.

Now, let's create another script that imports `my_`[`module.py`](http://module.py):

```python
# another_script.py

import my_module

print("This is another script.")
my_module.some_function()
```

When you run `another_`[`script.py`](http://script.py), the output will be:

```plaintext
This is another script.
Function in my_module
```

The `if __name__ == "__main__":` block is not executed when `my_`[`module.py`](http://module.py) is imported into `another_`[`script.py`](http://script.py), allowing you to have code that only runs when the script is the main program.

*This approach is commonly used to write reusable modules that can be both imported and run as standalone programs. The code inside the* `if __name__ == "__main__":` *block typically contains the main logic of the script when it is run independently.*

## Assert statement

The `assert` statement in Python is used to test if a given logical expression is `True`. If the expression is `False`, the `assert` statement raises an `AssertionError` exception with an optional error message.

The syntax of the `assert` statement is as follows:

```python
assert expression[, message]
```

* `expression`: A logical expression that is expected to be `True`.
    
* `message` (optional): An optional error message that is displayed when the assertion fails.
    

Here's a simple example:

```python
# Check if a list is not empty
my_list = []

assert my_list, "List should not be empty"

# The program continues if the list is not empty
print("List is not empty")
```

Here, `assert` statement checks if the list is not empty, and if it is, an `AssertionError` is raised.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">It's good practice to use <code>assert</code> for situations that should never occur in normal execution (e.g., invariant conditions) and to help catch bugs during development. However, in production code, it's better to rely on proper error handling mechanisms for robustness.</div>
</div>

## Q & A

Hope you have understood what are functions in python now it's your work to answer all these questions in the comment box to check your learning.

\* What is a function in Python?

\* How do you define a function in Python?

\* What is the purpose of the `def` keyword?

\* What is a function parameter?

\* How do you pass arguments to a function?

\* Explain the difference between formal parameters and actual arguments.

\* What is the purpose of the `return` statement in a function?

\* Can a function have multiple `return` statements?

\* What happens if a function doesn't have a `return` statement?

\* What are default parameters in a function?

\* How do you specify default values for function parameters?

\* Can you have both default and non-default parameters in a function?

\* What are variable-length arguments in Python functions?

\* Explain the use of `*args` and `**kwargs`.

\* Provide an example of a function using variable-length arguments.

## Conclusion

In this article, we've discussed Function Basics, Types of Arguments, Return Statement, `__name__` Variable, `assert` Statement and How to create functions. At the end, I also provided you guys with some questions to try it yourself. Feel free to drop a comment in case you have any doubt I'll make sure to help you. Keep learning Keep Growing.

*To stay updated on the upcoming articles, make sure to follow me and also don't forget to subscribe to my newsletter.*

*Your commitment to learning Python is commendable, and I'm excited to continue this journey with you. Thank you for being a part. Happy coding!💖*