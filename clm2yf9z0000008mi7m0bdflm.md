---
title: "Algorithm Design Techniques 101"
datePublished: Sun Sep 03 2023 04:30:09 GMT+0000 (Coordinated Universal Time)
cuid: clm2yf9z0000008mi7m0bdflm
slug: algorithm-design-techniques-101
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1693628647538/df865c40-3669-4d3f-8d5b-b39f44cdbedb.png
tags: algorithms, algorithm, design, computer-science, dsa

---

## Introduction

Welcome to the **first blog** in my **_algorithm design series_**! 🚀 In this series, I'll be sharing **various algorithm design techniques** that you _should_ use. You may _already_ know these, but still, I'll recommend you to **_read these articles once_**. You could at least give me a view. 😄 Jokes apart, in these articles, everything will be **_precise and to the point_**. So you could get the full value from these articles. Now, without further ado, let me give you a **_brief introduction_** about what all things I'll be covering in this series. In this article, I'll provide you with a **_brief introduction_** to the concepts, and in the upcoming articles, we'll **_delve deep into these concepts_**.

The various algorithm design techniques are:

1. **_Brute Force_**
    
2. **_Greedy Algorithms_**
    
3. **_Divide-and-Conquer, Decrease-and-Conquer_**
    
4. **_Dynamic Programming_**
    
5. **_Reduction / Transform-and-Conquer_**
    
6. **_Backtracking and Branch-and-Bound_**
    

## Brute Force Algorithm

The **brute force algorithm** is an approach that comes directly to our minds after viewing a problem. This is usually a straightforward approach based on the problem statement. We could use this approach to solve problems with small-sized datasets. Let me give you an example.

Let's say you want to find the **shortest path from your home to your school**. The **brute force solution** in this case would be to consider every possible combination of roads and intersections to reach your destination. However, this method is **_highly inefficient_**, especially if there are a lot of roads. I hope now you understand what I'm trying to say. 😅

Some examples of brute force algorithms are:

* **_Bubble-Sort_**
    
* **_Selection-Sort_**
    
* **_Sequential search in an array_**
    
* **_Computing pow(a, n) by multiplying a, n times_**
    
* **_Convex hull problem_**
    
* **_String matching_**
    
* **_Exhaustive search: Travelling salesman, Knapsack, etc._**
    

## Greedy Algorithm

**Greedy algorithms** are used to solve **optimization problems**. These problems usually involve finding the maximum or minimum of something from the given data. In a greedy algorithm, we find the solution through a sequence of steps. At each step, a choice is made that is **_locally optimal_**.

What does **_"locally optimal"_** mean?

First, we take a small part of the provided data, and then we find the **_optimal solution within that data_**. After that, we'll again take some data and repeat the process. Finding the optimal solution within the data we've considered is called **_locally optimal_**.

Some examples of greedy algorithms are:

* **_Minimal spanning tree: Prim's algorithm, Kruskal's algorithm_**
    
* **_Dijkstra's algorithm for single-source shortest path problem_**
    
* **_Greedy algorithm for the Knapsack problem_**
    
* **_The coin exchange problem_**
    
* **_Huffman trees for optimal encoding_**
    

## Divide-and-Conquer, Decrease-and-Conquer

In **_Divide-and-Conquer_** algorithms, as the name suggests, we first **_divide the problem into similar subproblems_**, and then we **_conquer each problem one by one_**. It involves three basic steps:

1. First, we **_divide the problem into similar sub-problems_**.
    
2. Then, we **_solve each one of these subproblems individually_**.
    
3. Finally, we **_combine the results of the subproblems to produce the desired result_**.
    

**Divide-and-Conquer** and **Decrease-and-Conquer** are very similar, but they have a slight difference between them. In divide and conquer, the size of the problem is reduced by a factor (half, one third, etc.), while in decrease and conquer, the size of the problem is reduced by a constant.

Some examples of divide-and-conquer algorithms are:

* **_Merge-Sort algorithm (using recursion)_**
    
* **_Quick sort algorithm (using recursion)_**
    
* **_Computing the length of the longest path in a binary tree (using recursion)_**
    
* **_Computing Fibonacci numbers (using recursion)_**
    
* **_Quick-hull_**
    

Some examples of decrease-and-conquer algorithms are:

* **_Computing pow(a, n) by calculating pow(a, n/2) using recursion_**.
    
* **_Binary search in a sorted list (using recursion)_**
    
* **_Searching in BST_**
    
* **_Insertion-Sort_**
    
* **_Graph traversal algorithms (DFS and BFS)_**
    
* **_Topological sort_**
    
* **_Warshall’s algorithm (using recursion)_**
    
* **_Permutations (Minimal change approach, Johnson-Trotter algorithm)_**
    
* **_Computing a median, Topological sorting, Fake-coin problem (Ternary search)_**
    

## Dynamic Programming

In divide and conquer, many times the recursively solved subproblems can result in the same computation being performed multiple times. This problem arises when identical problems occur repeatedly in a recursion.

**Dynamic programming** is used to avoid this issue by storing the results of subproblems in a table and referring to that table to check if we have already calculated the solution to a subproblem before computing it again.

Dynamic programming is a **_bottom-up technique_** in which the smaller subproblems are solved first, and the results of these are used to find the solution for larger subproblems.

Some examples of Dynamic programming are:

* **_Fibonacci numbers computed by iteration._**
    
* **_Warshall’s algorithm for transitive closure implemented by iterations._**
    
* **_Floyd’s algorithm for all-pairs shortest paths._**
    

## Reduction / Transform-and-Conquer

These methods work as a **_two-step process_**. First, the problem is transformed into a different problem that is already known to us, i.e., a problem for which we already know the optimal solution. Then the problem is solved.

The most common type of transformation is the **_sorting of an array_**.

For example, in a given list of numbers, find the two closest numbers. In the brute-force solution, we would find the distance between each element in the array and keep track of the pair with the minimum distance. In this approach, the total time complexity is **_O(n^2)_**. In the Transform and Conquer solution, we first sort the array in **_O(n log n)_** time and then find the closest numbers by scanning the array in another single pass with time complexity **_O(n)_**. Thus, the total time complexity is **_O(n log n)_**.

Some examples of

 Transform and Conquer are:

* **_Gaussian elimination_**
    
* **_Heaps and Heapsort_**
    

## Backtracking

Have you seen the modern lock with a 3-digit password, where the numbers range from 1 to 9? If you don't have the exact password for the lock, you need to test every combination until you find the right one. You would go from something like "111" to "112" and so on until you reach "999". In this case, what you are doing is called **_backtracking_**.

Suppose the lock produces a click sound anytime you come across a correct digit. If we can listen to this sound, it will help you reach the goal much faster. These functions are called **_Pruning functions or Bounding functions_**.

Backtracking is a method in which a solution is found by searching through a large but finite number of states. With some **_pruning or bounding functions_**, we can narrow down our search.

For all problems (like NP-hard problems) for which there does not exist any other efficient algorithm, we use the **_backtracking algorithm_**.

Backtracking problems have the following components:

* **_Initial state_**
    
* **_Target/Goal state_**
    
* **_Intermediate states_**
    
* **_Path from the initial state to the target/goal state_**
    
* **_Operators to get from one state to another_**
    
* **_Pruning function (optional)_**
    

The algorithm starts with the construction of a **_state tree_**, whose nodes represent the states. The root node is the initial state, and one or more leaf nodes will be our target state. Each edge of the tree represents some operation. The solution is obtained by searching the tree until a target is found.

### Some real-life problems where you could use the backtracking approach are:

1. **_Three Monks and Three Demons_**: There are three monks and three demons on one side of a river. You want to move all of them to the other side using a small boat. The boat can carry only two persons at a time. If, on any shore, the number of demons is more than the number of monks, the demons will eat the monks. How can we move all of these people to the other side of the river safely?
    
2. **_The Farmer's Dilemma_**: There is a farmer who has a goat, a cabbage, and a wolf. If the farmer leaves the goat with the cabbage, the goat will eat the cabbage. If the farmer leaves the wolf alone with the goat, the wolf will kill the goat. How can the farmer move all his belongings to the other side of the river?
    
3. **_Jug Problem_**: You are given two jugs, a 4-gallon one and a 3-gallon one. There are no measuring markers on the jugs. A tap can be used to fill the jugs with water. How can you get 2 gallons of water in the 4-gallon jug?
    

## Branch-and-bound

The **_branch and bound method_** is used when we can evaluate the cost of visiting each node using a utility function. At each step, we choose the node with the lowest cost to proceed further. Branch-and-bound algorithms are implemented using a priority queue. In branch and bound, we traverse the nodes in a breadth-first manner.

## A\* Algorithm

**_A\*_** is an extension of the branch and bound approach. In A\*, we select the path with the shortest length from the start to the goal. The total length is estimated as the length traversed so far plus a heuristic estimate of the remaining distance from the goal.

Branch-and-bound will always find an optimal solution, which is the shortest path. A\* will also find an optimal solution if the heuristic is accurate. Choosing a good heuristic is the most crucial aspect of the A\* algorithm.

## Conclusion

Usually, any problem can be solved using a variety of methods. However, we shouldn't always settle for the first method that comes to mind, such as brute force. Some methods yield much more efficient solutions than others. That's why it's necessary to be acquainted with all available methods.

Now, you might wonder how to choose the best method.

First, you should thoroughly comprehend the problem statement.

Second, by being familiar with various problems and their solutions, you can then refine your approach.

**_Ready to Dive Deeper? Explore the Rest of the Series for In-Depth Algorithm Insights. Don't Miss Out – Subscribe to Our Newsletter for Updates on Future Articles!_** [**_Subscribe here_**](https://coolcoderr.hashnode.dev/newsletter)**.**

Happy Coding ❤️