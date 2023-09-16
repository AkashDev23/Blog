---
title: "Understanding Dynamic Programming in Algorithms"
datePublished: Sat Sep 16 2023 08:39:11 GMT+0000 (Coordinated Universal Time)
cuid: clmls1m8n001909mk36hm09hi
slug: understanding-dynamic-programming-in-algorithms
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693657069727/ced63c0d-e066-4812-a7b2-a968c7a7d364.png
tags: python, dsa, dynamic-programming, python-beginner, fibonacci

---

Welcome to the fourth article of our Algorithm Design Series! In this blog post, we dive into the world of Dynamic Programming (DP) which is a powerful technique used in algorithm design to optimize problem-solving by avoiding redundant calculations. It's particularly handy when dealing with problems exhibiting two key properties: Optimal Substructure and Overlapping Sub-problems.

But before that, it's very necessary to understand what exactly DP is.

## **What is Dynamic Programming?**

Dynamic programming is a problem-solving technique that helps us avoid the repetition of calculations by storing the results of sub-problems in a data structure (often a table) for future reference. This approach significantly improves efficiency and is commonly applied to solve problems in various domains.

### **Key Properties for Applying Dynamic Programming**

To determine if Dynamic Programming is suitable for a given problem, we need to check for the following properties:

1. **Optimal Substructure:** The problem should exhibit an optimal solution constructed from the optimal solutions of its sub-problems.
    
2. **Overlapping Sub-problems:** During the calculation of optimal solutions for sub-problems, the same computations should be repeated multiple times.
    

### **Steps to Apply Dynamic Programming**

To effectively use Dynamic Programming, follow these steps:

1. **Optimal Substructure:** Identify if there's a recursive relation between the main problem and its sub-problems.
    
2. **Write Recursive Relations:** Write down the recursive relation of the problem, paying attention to potential overlapping sub-problems.
    
3. **Compute Sub-problems:** Calculate the values of sub-problems in a bottom-up fashion, storing these values in a data structure.
    
4. **Construct the Optimal Solution:** Build the optimal solution using the values stored in step 3.
    
5. **Repeat:** Continue steps 3 and 4 until you arrive at the final solution.
    

## **Examples of Problems Solved Using Dynamic Programming**

Dynamic Programming is a versatile technique applied to a wide range of problems. Let's explore some classic examples:

### **1\. Fibonacci Numbers**

**Explanation:** The Fibonacci sequence is a series of numbers where each number is the sum of the two preceding ones: 0, 1, 1, 2, 3, 5, 8, 13, ...

**Code:**

```python
def fibonacci(n):
    if n <= 1:
        return n
    fib = [0] * (n + 1)
    fib[1] = 1
    for i in range(2, n + 1):
        fib[i] = fib[i - 1] + fib[i - 2]
    return fib[n]
```

**Time Complexity:** O(n) **Space Complexity:** O(n)

**Explanation:** In this example, we use an array to store the Fibonacci numbers to avoid redundant calculations. The time complexity is linear because we calculate each Fibonacci number from 2 to n once. The space complexity is also linear because we store all Fibonacci numbers up to n in an array.

### **2\. Assembly-line Scheduling**

**Explanation:** Assembly-line scheduling is a problem in which we optimize the time needed to build a product using multiple assembly lines. It involves finding the fastest way to assemble a product while considering entry and exit times for each assembly line.

**Code:** The code for this problem is complex and involves multiple arrays and dynamic programming techniques. It's beyond the scope of a single code snippet. That's why I am not providing it here but you can check it by clicking on this [link](https://www.geeksforgeeks.org/assembly-line-scheduling-dp-34/).

**Time Complexity:** O(n) **Space Complexity:** O(n)

**Explanation:** The time and space complexity for assembly-line scheduling can vary depending on the specific problem instance and the algorithm used. In general, it can have a time complexity of O(n) and space complexity of O(n) when implemented efficiently.

### **3\. Longest Increasing Subsequence**

**Explanation:** The Longest Increasing Subsequence problem involves finding the longest subsequence in an array where elements are in increasing order but not necessarily contiguous.

**Code:**

```python
def longest_increasing_subsequence(arr):
    n = len(arr)
    lis = [1] * n
    for i in range(1, n):
        for j in range(i):
            if arr[i] > arr[j] and lis[i] < lis[j] + 1:
                lis[i] = lis[j] + 1
    return max(lis)
```

**Time Complexity:** O(n^2) **Space Complexity:** O(n)

**Explanation:** In this code, we use dynamic programming to find the length of the longest increasing subsequence in the given array. The time complexity is O(n^2) because we have a nested loop. The space complexity is O(n) as we use an additional array to store the lengths of increasing subsequences.

### **4\. Matrix Chain Multiplication**

**Explanation:** The Matrix Chain Multiplication problem involves finding the most efficient way to multiply a sequence of matrices to minimize the number of operations required.

**Code:**

```python
def matrix_chain_multiplication(dims):
    n = len(dims) - 1
    dp = [[0] * n for _ in range(n)]
    for chain_length in range(2, n + 1):
        for i in range(n - chain_length + 1):
            j = i + chain_length - 1
            dp[i][j] = float('inf')
            for k in range(i, j):
                cost = dp[i][k] + dp[k + 1][j] + dims[i] * dims[k + 1] * dims[j + 1]
                dp[i][j] = min(dp[i][j], cost)
    return dp[0][n - 1]
```

**Time Complexity:** O(n^3) **Space Complexity:** O(n^2)

**Explanation:** The code above uses dynamic programming to solve the Matrix Chain Multiplication problem efficiently. The time complexity is O(n^3), where n is the number of matrices. The space complexity is O(n^2) due to the DP table.

### **5\. Longest Common Subsequence**

**Explanation:** The Longest Common Subsequence (LCS) problem involves finding the longest subsequence common to two sequences.

**Code:**

```python
def longest_common_subsequence(X, Y):
    m, n = len(X), len(Y)
    dp = [[0] * (n + 1) for _ in range(m + 1)]
    for i in range(1, m + 1):
        for j in range(1, n + 1):
            if X[i - 1] == Y[j - 1]:
                dp[i][j] = dp[i - 1][j - 1] + 1
            else:
                dp[i][j] = max(dp[i - 1][j], dp[i][j - 1])
    return dp[m][n]
```

**Time Complexity:** O(m *n)* ***Space Complexity:*** *O(m* n)

**Explanation:** This code calculates the length of the longest common subsequence between two sequences X and Y using dynamic programming. The time complexity is O(m *n), where m and n are the lengths of the input sequences. The space complexity is also O(m* n) due to the DP table.

### **6\. Coin Exchange Problem**

**Explanation:** The Coin Exchange problem involves finding the minimum number of coins needed to make a change for a given amount using a set of coin denominations.

**Code:**

```python
def coin_exchange(coins, amount):
    dp = [float('inf')] * (amount + 1)
    dp[0] = 0
    for coin in coins:
        for i in range(coin, amount + 1):
            dp[i] = min(dp[i], dp[i - coin] + 1)
    return dp[amount] if dp[amount] != float('inf') else -1
```

**Time Complexity:** O(amount \* num\_coins) **Space Complexity:** O(amount)

**Explanation:** The code above uses dynamic programming to solve the Coin Exchange problem efficiently. The time complexity is O(amount \* num\_coins), where the amount is the target amount and num\_coins is the number of coin denominations. The space complexity is O(amount) due to the DP array.

These examples illustrate how Dynamic Programming can be applied to solve a variety of problems efficiently, making it a powerful technique in algorithm design.

## Conclusion

Through this article, we've explored the magic of Dynamic Programming through some examples, witnessing how it optimizes Fibonacci computations, streamlines assembly-line scheduling, and unlocks the secrets of longest subsequences and more.

But this is not the end of our journey. To delve deeper into the world of algorithm design techniques, I would love to recommend that you read our previous articles in this series. There's a lot waiting for you.

🚀 **Read the Previous Articles:** Dive into the algorithmic archives by reading our previous articles in the Algorithm Design Series. [**Explore Now**](https://coolcoderr.hashnode.dev/series/algo-design)

💌 **Subscribe to Our Newsletter:** Stay in the algorithmic loop with our newsletter. Get updates, tips, and more delivered straight to your inbox. [**Subscribe Here**](https://coolcoderr.hashnode.dev/newsletter)

Happy Coding!