---
title: "Demystifying Python Namespaces"
datePublished: Sat Dec 30 2023 04:41:09 GMT+0000 (Coordinated Universal Time)
cuid: clqrkry0u000608l2emzoe3dq
slug: demystifying-python-namespaces
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703017119163/9008b3b2-e00b-4bcc-a91b-f1ed8a83b523.png
tags: python, beginner, python3, beginners, python-beginner, python-projects

---

Hey everyone, Welcome to the new article of Python Foundations for Beginners Series. In this article, we are going to cover a small yet very important topic Namespace. So without further ado, let's start.

In Python, a namespace is a container that holds a mapping of names to objects. It provides a way to organize and manage names in a program to avoid naming conflicts and to enable code to be modular and maintainable. Python uses namespaces to keep track of variables, functions, classes, and other objects, and it helps avoid naming collisions between different parts of a program.

There are several types of namespaces in Python, including:

1. **Local Namespace:** This namespace includes names that are defined within a function or a method. It is temporary and exists only during the execution of that specific function or method.
    
    ```python
    def example_function():
        local_variable = 42
        print(local_variable)
    
    example_function()
    ```
    
    In this example, `local_variable` is part of the local namespace of the `example_function`.
    
2. **Global Namespace:** This namespace contains names defined at the top level of a script or module. It is accessible throughout the entire module.
    
    ```python
    global_variable = 100
    
    def another_function():
        print(global_variable)
    
    another_function()
    ```
    
    Here, `global_variable` is part of the global namespace.
    
3. **Built-in Namespace:** This namespace includes names that are built into the Python language and are always available. Examples include functions like `print()` and built-in types like `int` and `str`.
    
    ```python
    print("Hello, World!")
    ```
    
    In this case, `print` is part of the built-in namespace.
    
4. **Enclosing Namespace:** This namespace is specific to nested functions or classes. If a function is defined within another function, it has access to its own local namespace, the local namespace of the outer function, and the global namespace.
    
    ```python
    def outer_function():
        outer_variable = 50
    
        def inner_function():
            print(outer_variable)
    
        inner_function()
    
    outer_function()
    ```
    
    Here, `outer_variable` is part of the enclosing namespace for `inner_function`.
    

I hope namespace was clear to you all. In the next article, I'll be talking about Strings so before that practice and revise all these topics coverted till now.

*For more such articles, subscribe to our newsletter. Keep learning keep growing.*