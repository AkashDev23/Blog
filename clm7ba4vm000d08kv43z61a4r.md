---
title: "Brute Force Algorithms: The Power of Exhaustive Search"
datePublished: Wed Sep 06 2023 05:41:09 GMT+0000 (Coordinated Universal Time)
cuid: clm7ba4vm000d08kv43z61a4r
slug: brute-force-algorithms-the-power-of-exhaustive-search
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693550241594/83d1226a-75b5-4446-8c7e-505f23934d97.png
tags: algorithms, java, design, dsa, bruteforcing

---

Hey there, readers! 👋 This is the second article in my blog series, where we'll explore problems that can be solved using **brute-force algorithms**. In the previous article, I introduced this algorithm. If you haven't read it yet, please go check it out and then come back to this one. [**Link to the previous article**](https://coolcoderr.hashnode.dev/series/algo-design)

## Bubble Sort

**Bubble Sort** is an algorithm where adjacent elements of an array are compared and exchanged if they are out of order.

```java
public static void bubbleSort(int[] arr) {
        int n = arr.length;
        boolean sorted = false;
        while (!sorted) {
            sorted = true;
            for (int j = 0; j < n - 1; j++) {
                if (arr[j] > arr[j + 1]) {
                    // Swap the elements if they are out of order.
                    int temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                    sorted = false;
                }
            }
        }
    }
```

The time complexity is **Θ(n^2)**.

## Selection Sort

In **Selection Sort**, the entire given list of N elements is traversed to find its smallest element and exchange it with the first element. This process is repeated until the array is completely sorted.

```java
public static void selectionSort(int[] arr) {
        int n = arr.length;
        for (int i = 0; i < n - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[minIndex]) {
                    // Find the index of the minimum element.
                    minIndex = j;
                }
            }
            // Swap the minimum element with the current element.
            int temp = arr[i];
            arr[i] = arr[minIndex];
            arr[minIndex] = temp;
        }
    }
```

The time complexity is **O(n^2)**.

## Sequential Search

**Sequential Search** is an algorithm that compares consecutive elements of a given list with a search keyword until a match is found or the array is exhausted.

```java
public static int sequentialSearch(int[] arr, int key) {
        int n = arr.length;
        for (int i = 0; i < n; i++) {
            if (arr[i] == key) {
                // Return the index if the key is found.
                return i;
            }
        }
        // Return -1 if the key is not found.
        return -1;
    }
```

The worst-case time complexity is **Θ(n)**.

## Computing pow(a, n)

Computing **a^n** (**a** &gt; 0, and **n** is a nonnegative integer) based on the definition of exponentiation. The brute-force method requires N-1 multiplications.

```java
    public static double power(double a, int n) {
        double result = 1.0;
        for (int i = 0; i < n; i++) {
            result *= a;
        }
        return result;
    }
```

The algorithm requires **Θ(n)**.

## String Matching

A brute force string matching algorithm takes two inputs: a text consisting of n characters and a pattern consisting of m characters (m ≤ n). The algorithm compares the pattern with the text, character by character, starting from left to right until all characters match or a mismatch is found. This process is repeated until a match is found, starting from each position in the text.

```java
    public static int bruteForceStringMatch(String text, String pattern) {
        int n = text.length();
        int m = pattern.length();
        for (int i = 0; i <= n - m; i++) {
            int j;
            for (j = 0; j < m; j++) {
                if (text.charAt(i + j) != pattern.charAt(j)) {
                    break;
                }
            }
            if (j == m) {
                // Pattern found at index i in the text.
                return i;
            }
        }
        // Pattern not found in the text.
        return -1;
    }
```

In the worst case, the algorithm is **O(mn)**.

## Closest Pair Brute-Force Algorithm

The closest-pair problem involves finding the two closest points in a set of n points in a 2-dimensional space. A brute-force implementation computes the distance between each pair of distinct points and finds the smallest distance pair.

```java
    public static double closestPair(int[] x, int[] y) {
        int n = x.length;
        double minDistance = Double.POSITIVE_INFINITY;
        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                double distance = Math.sqrt(Math.pow(x[i] - x[j], 2) + Math.pow(y[i] - y[j], 2));
                if (distance < minDistance) {
                    minDistance = distance;
                }
            }
        }
        return minDistance;
    }
```

The time complexity is **Θ(n^2)**.

## Convex Hull Problem

The convex hull of a set of points is the smallest convex polygon that contains all the points. The convex hull includes points on its boundary or inside it.

To find this subset, we identify the boundary points of the convex hull. We take any two consecutive points on the boundary, and all the other points lie on one side of the line connecting these two points. For each of n(n-1)/2 pairs of distinct points, we check whether all other points lie on the same side of the line.

The worst-case cost of the algorithm is **O(n^3)**.

```java
    public static void convexHull(int[] x, int[] y) {
        int n = x.length;
        for (int i = 0; i < n - 1; i++) {
            for (int j = i + 1; j < n; j++) {
                int a = y[i] - y[j];
                int b = x[j] - x[i];
                int c = x[i] * y[j] - x[j] * y[i];
                boolean allOnOneSide = true;
                for (int k = 0; k < n; k++) {
                    if (k != i && k != j) {
                        int side = a * x[k] + b * y[k] - c;
                        if (side > 0) {
                            allOnOneSide = false;
                            break;
                        }
                    }
                }
                if (allOnOneSide) {
                    System.out.println("Line from (" + x[i] + ", " + y[i] + ") to (" + x[j] + ", " + y[j] + ") is on the convex hull.");
                }
            }
        }
    }
```

## Exhaustive Search

Exhaustive search is a brute-force approach applied to combinatorial problems. It generates all possible combinations and checks if they satisfy problem constraints.

Examples of exhaustive search problems include the **Traveling Salesman Problem**, the **Knapsack Problem**,

and the **Assignment Problem**.

### Traveling Salesman Problem (TSP)

In the **Traveling Salesman Problem**, we need to find the shortest tour through a set of N cities, visiting each city exactly once before returning to the starting city. This is equivalent to finding the shortest Hamiltonian circuit in a weighted connected graph. To solve it, we generate all permutations of cities and calculate the length of each path.

The total number of possible combinations is **(n-1)!** The cost of calculating each path is **Θ(n)**. Therefore, the total cost of finding the shortest path is **Θ(n!)**.

### Knapsack Problem

Given items with costs C1, C2, ..., Cn, volumes V1, V2, ..., Vn, and a knapsack of capacity Vmax, we aim to find the most valuable set of items that fit in the knapsack. This problem involves considering all possible subsets of objects, which results in a time complexity of **O(2^n)**.

```java
Algorithm KnapsackBruteForce
MaxProfit =

 0
For (All permutations of objects) do
CurrProfit = sum of selected objects
If (MaxProfit < CurrProfit)
MaxProfit = CurrProfit
Store the current set of selected objects
```

## Conclusion

**Brute force algorithms** are often the first choice when facing a problem. They are simple to understand but may not always provide the most efficient solution. In many cases, more effective algorithms can be found that outperform brute force methods.

Subscribe to our newsletter for the latest articles in our series. Don't miss out—get notified! [**Subscribe Now**](https://coolcoderr.hashnode.dev/newsletter) 👈📩