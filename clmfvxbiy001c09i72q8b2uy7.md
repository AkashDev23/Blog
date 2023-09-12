---
title: "Divide and Conquer 101"
datePublished: Tue Sep 12 2023 05:41:12 GMT+0000 (Coordinated Universal Time)
cuid: clmfvxbiy001c09i72q8b2uy7
slug: divide-and-conquer-101
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693636476476/73b48c36-571c-49f8-ae6d-1a7caf4a380a.png
tags: algorithms, python, dsa, python-beginner, divide-and-conquer

---

Hey dear readers! 👋 Hope you are enjoying the algorithm design blog series so far. We've covered some basics and problems on brute force and greedy algorithms. In this blog, we'll dive into the world of **divide-and-conquer** and **decrease-and-conquer** algorithms. Let's also see how to solve their problems. Without further ado, let's get started! 📖

## Divide and Conquer at a Glance 🧩

Divide-and-conquer algorithms work by recursively breaking down a problem into two or more sub-problems (divide step) until these sub-problems become simple enough to be solved directly (conquer step). The solution of these sub-problems is then combined to give a solution to the original problem.

**Divide-and-conquer algorithms involve three basic steps:**

1. **Divide:** Divide the problem into smaller problems.
    
2. **Conquer:** Solve these problems.
    
3. **Combine:** Combine these results.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693639501016/b470ee1b-42a9-457e-9589-6936784ac902.png align="center")

In **divide-and-conquer**, the size of the problem is reduced by a factor (half, one-third, etc.), while in **decrease-and-conquer**, the size of the problem is reduced by a constant.

## Examples of Divide-and-Conquer Algorithms 🌟

### Divide and Conquer:

* Merge-Sort algorithm (recursion)
    
* Quicksort algorithm (recursion)
    
* Computing the length of the longest path in a binary tree (recursion)
    
* Computing Fibonacci numbers (recursion)
    
* Convex Hull
    

### Decrease and Conquer:

* Computing POW (a, n) by calculating POW (a, n/2) using recursion
    
* Binary search in a sorted list (recursion)
    
* Searching in BST
    
* Insertion-Sort
    
* Graph traversal algorithms (DFS and BFS)
    
* Topological sort
    
* Warshall’s algorithm (recursion)
    
* Permutations (Minimal change approach, Johnson-Trotter algorithm)
    
* Fake-coin problem (Ternary search)
    
* Computing a median
    

## General Divide-and-Conquer Recurrence 📊

The general recurrence for divide-and-conquer is defined as:

T(n) = aT(n/b) + f(n)

Where:

* "a" is the number of sub-problems in the recursion.
    
* "n" is the size of a problem.
    
* "b" is a factor by which the size of the problem is reduced.
    
* "f(n)" is the cost of dividing the problem into sub-problems or merging the results.
    

## Problems on Divide-and-Conquer Algorithm 🤔

### Merge-Sort Algorithm

Merge Sort is a popular comparison-based sorting algorithm that follows the divide-and-conquer paradigm. Here's a brief explanation of how it works:

1. **Divide:** Divide the unsorted array into two halves until each subarray contains only one element.
    
2. **Conquer:** Merge the subarrays in a sorted manner. Start by comparing the elements in the two subarrays, and merge them into a single sorted array.
    
3. **Repeat:** Continue dividing and merging until the entire array is sorted.
    

**Time Complexity:**

* Best Case: O(n log n)
    
* Average Case: O(n log n)
    
* Worst Case: O(n log n)
    

**Space Complexit**y: O(n)

Here's a Python implementation of Merge Sort:

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr

    mid = len(arr) // 2
    left_half = arr[:mid]
    right_half = arr[mid:]

    left_half = merge_sort(left_half)
    right_half = merge_sort(right_half)

    return merge(left_half, right_half)

def merge(left, right):
    result = []
    i = j = 0

    while i < len(left) and j < len(right):
        if left[i] < right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1

    result.extend(left[i:])
    result.extend(right[j:])

    return result

# Usage
arr = [12, 11, 13, 5, 6, 7]
sorted_arr = merge_sort(arr)
print(sorted_arr)
```

### Quick Sort **Algorithm**

Quick Sort is another popular comparison-based sorting algorithm that also uses the divide-and-conquer approach. Here's a brief explanation:

1. **Partition:** Select a pivot element from the array and partition the other elements into two subarrays, according to whether they are less than or greater than the pivot.
    
2. **Recursion:** Recursively apply the quick sort algorithm to the two subarrays.
    
3. **Combine:** Combine the sorted subarrays and the pivot element to obtain the final sorted array.
    

**Time Complexity:**

* Best Case: O(n log n)
    
* Average Case: O(n log n)
    
* Worst Case: O(n^2) (rare, but can occur)
    

**Space Complexity:** O(nlogn)

Here's a Python implementation of Quick Sort:

```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr

    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]

    return quick_sort(left) + middle + quick_sort(right)

# Usage
arr = [12, 11, 13, 5, 6, 7]
sorted_arr = quick_sort(arr)
print(sorted_arr)
```

### Binary Search

Binary Search is a search algorithm that works on sorted arrays by repeatedly dividing the search interval in half. Here's a brief explanation:

1. **Initialize:** Start with the entire sorted array.
    
2. **Compare:** Compare the middle element with the target value.
    
3. **Update Interval:** If the middle element is greater than the target, search in the left half; if it's smaller, search in the right half.
    
4. **Repeat:** Continue the process until the target is found or the interval becomes empty.
    

**Time Complexity:**

* Average and Worst Case: O(log n)
    

Here's a Python implementation of Binary Search:

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1

    while left <= right:
        mid = (left + right) // 2

        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1

    return -1  # Target not found

# Usage
arr = [2, 3, 4, 10, 40]
target = 10
result = binary_search(arr, target)
if result != -1:
    print(f"Element found at index {result}")
else:
    print("Element not found")
```

| Algorithm | Worst Case Time Complexity | Average Case Time Complexity | Space Complexity |
| --- | --- | --- | --- |
| Merge-Sort | O(nlogn) | O(nlogn) | O(n) |
| Quick-Sort | O(n^2) | O(nlogn) | O(nlogn) |
| Binary Search | O(logn) | O(logn) | O(1) |

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1693639528334/576957ce-847d-48a0-bfd0-1746479cccdd.png align="center")

And more...

## Power Function, Convex Hull, Closest Pair, and External Sorting 🌐

These topics and algorithms, such as the power function, convex hull, closest pair, and external sorting, also employ the divide-and-conquer technique to efficiently solve various problems.

### **Power Function (Exponentiation):**

Calculate the result of raising a number to an exponent.

1. **Base Case:** If the exponent is 0, return 1 (any number raised to the power of 0 is 1).
    
2. **Recursion:** For positive exponents, recursively multiply the base by the result of the power function with a reduced exponent.
    
3. **Optimization:** For negative exponents, calculate the reciprocal of the base and negate the exponent to find the result.
    

* Time Complexity: O(log n) using recursive exponentiation.
    

Python Code:

```python
def power(base, exponent):
    if exponent == 0:
        return 1
    elif exponent < 0:
        base = 1 / base
        exponent = -exponent

    if exponent % 2 == 0:
        half_pow = power(base, exponent // 2)
        return half_pow * half_pow
    else:
        half_pow = power(base, (exponent - 1) // 2)
        return half_pow * half_pow * base

# Usage
base = 2
exponent = 4
result = power(base, exponent)
print(f"{base}^{exponent} = {result}")
```

### **Convex Hull:**

Find the smallest convex polygon containing a set of points.

1. **Sort Points:** Sort the points by their x-coordinates (and y-coordinates for tie-breaking if needed).
    
2. **Find Hull:** Use a convex hull algorithm (e.g., Graham's Scan or Jarvis March) to find the convex hull of the sorted points.
    
3. **Return Hull:** The convex hull is the final result.
    

* Time Complexity: O(n log n) for sorting, O(nh) for finding the convex hull.
    

```python
from scipy.spatial import ConvexHull

points = [(0, 3), (2, 2), (1, 1), (2, 1), (3, 0), (0, 0), (3, 3)]
hull = ConvexHull(points)
hull_points = [points[i] for i in hull.vertices]

print("Convex Hull Points:", hull_points)
```

### **Closest Pair of Points:**

The closest Pair of Points problem is to find the two points in a set of points that are closest to each other. Here's a brief explanation:

1. **Sort by X:** Sort the points by their x-coordinates.
    
2. **Divide and Conquer:** Divide the sorted points into two halves along the median x-coordinate. Recursively find the closest pair in each half.
    
3. **Merge Step:** After finding the closest pairs in each half, consider pairs where one point is in the left half and the other in the right half, within a certain strip of width 2\*delta around the median. Find the closest pair in this strip.
    
4. **Return Minimum:** Return the minimum distance among all these pairs.
    

* Time Complexity: O(n log n) using a divide-and-conquer approach.
    

Python Code:

```python
import math

def closest_pair(points):
    # Sort points by x-coordinate
    points.sort(key=lambda x: x[0])

    def distance(p1, p2):
        return math.sqrt((p1[0] - p2[0])**2 + (p1[1] - p2[1])**2)

    def closest_pair_recursive(points):
        if len(points) <= 3:
            return min(points, key=lambda x: x[0]), min(points, key=lambda x: x[1])

        mid = len(points) // 2
        left_half = points[:mid]
        right_half = points[mid:]

        left_closest = closest_pair_recursive(left_half)
        right_closest = closest_pair_recursive(right_half)

        delta = min(distance(left_closest[0], left_closest[1]), distance(right_closest[0], right_closest[1]))
        strip = [point for point in points if abs(point[0] - points[mid][0]) < delta]

        strip_closest = None
        min_strip_distance = delta

        for i in range(len(strip)):
            for j in range(i + 1, len(strip)):
                if abs(strip[i][1] - strip[j][1]) < delta:
                    d = distance(strip[i], strip[j])
                    if d < min_strip_distance:
                        min_strip_distance = d
                        strip_closest = (strip[i], strip[j])

        if strip_closest:
            return strip_closest
        elif distance(left_closest[0], left_closest[1]) < distance(right_closest[0], right_closest[1]):
            return left_closest
        else:
            return right_closest

    return closest_pair_recursive(points)

# Usage
points = [(2, 3), (12, 30), (40, 50), (5, 1), (12, 10), (3, 4)]
closest = closest_pair(points)
print("Closest Pair of Points:", closest)
```

### **External Sorting:**

External Sorting is a technique for sorting large datasets that don't fit entirely in memory. It involves dividing the data into smaller chunks, sorting them in memory, and then merging the sorted chunks to produce the final sorted dataset.

* Time Complexity: O(n log n), where 'n' is the size of the dataset.
    

Python Code (simplified example):

```python
import heapq

def external_sort(input_filename, output_filename, chunk_size):
    with open(input_filename, 'rb') as infile, open(output_filename, 'wb') as outfile:
        # Read and sort chunks in memory
        chunk = []
        for line in infile:
            chunk.append(line)
            if len(chunk) >= chunk_size:
                chunk.sort()
                outfile.writelines(chunk)
                chunk = []

        # Sort and write any remaining data in memory
        chunk.sort()
        outfile.writelines(chunk)

# Usage
input_file = "unsorted_data.txt"
output_file = "sorted_data.txt"
chunk_size = 10000
external_sort(input_file, output_file, chunk_size)
```

Please note that these are simplified code examples, and real-world implementations may require additional considerations and optimizations.

## Conclusion 🎉

Divide-and-conquer algorithms provide powerful tools for solving complex problems efficiently. They break down problems into manageable parts, conquer them individually, and then combine the solutions. Whether it's sorting, searching, or solving geometric problems, divide and conquer has got you covered! 🙌

Stay tuned for more algorithmic adventures in our blog series! Happy coding! 💻✨