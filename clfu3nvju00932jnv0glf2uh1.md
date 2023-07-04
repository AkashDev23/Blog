---
title: "My first coding test"
datePublished: Wed Mar 29 2023 19:48:39 GMT+0000 (Coordinated Universal Time)
cuid: clfu3nvju00932jnv0glf2uh1
slug: my-first-coding-test
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/Hcfwew744z4/upload/1b4dc2c1c8df56d1b42b3632f90e784c.jpeg
tags: test, hashnode, samsung, dfs, wemakedevs

---

Recently, I took my first online coding test, which was conducted by Samsung Prism. The question posed to me was not overly difficult, but it did require a considerable amount of thought. After working on it for about 20 minutes, I was able to find a solution.

In this blog post, I will be sharing that question and my approach to solving it.

*I chose to write the code in Java because it is the language I am most comfortable with. If you have a different solution or a code implementation in another language, please feel free to share it in the comments.*

# 🏠💻Finding the Largest House Group in a Matrix

## Question

> You are given a matrix of size n\*m. Each matrix element is either 0 or 1. 1 denotes that there is a House and 0 denotes there is a Park. You have to determine the largest house group or one that has a maximum number of neighbors. The neighbor of the house at position (i,j) will be the house at positions (i, j+1), (i, j-1), (i-1, j), (i+1, j).
> 
> For a better understanding see Sample Testcase.
> 
> **Input Format**
> 
> First-line contains an integer n denoting the number of rows. The next line contains an integer m denoting the number of columns. Next, n lines contain m space-separated matrix values i.e. either 0 or 1. Constraints
> 
> 1 &lt;= n,m &lt;= 2000 matrix\[i\]\[j\] can be 0 or 1. Output Format
> 
> Print the biggest neighbor size. Evaluation Parameter
> 
> **Sample Input**
> 
> 4 5 0 1 0 0 1 1 0 1 0 0 1 1 1 1 0 0 0 0 1 1
> 
> **Sample Output**
> 
> 8
> 
> **Explanation**
> 
> There are 3 groups:
> 
> \[\[0,1\]\] \[ \[1,0\], \[2,0\], \[2,1\], \[2,2\], \[1,2\], \[2,3\], \[3,3\], \[3,4\]\] \[\[0,4\]\] The biggest group among these 3 are \[\[1,0\], \[2,0\], \[2,1\], \[2,2\], \[1,2\], \[2,3\], \[3,3\], \[3,4\]\]. Whose size is 8.
> 
> Execution time limit 10 seconds

This was the exact question they asked. I would request you all to once try it yourself before reading it further and jumping into the solution.

## Our approach

The best way to solve the problem is to traverse the matrix and perform a depth-first search (DFS) to count the size of each house group. We can start with any unvisited house and visit its neighbors recursively until there are no more unvisited houses in the group. We keep track of the maximum size seen so far and return it as the answer.

### Steps of algorithm

1. Initialize a variable 'max\_size' to 0 and a boolean array 'visited' to keep track of visited cells.
    
2. Traverse the matrix and search for houses.
    
3. If the current cell is a house and is not visited, perform a DFS search to count the size of the house group.
    
4. Update the maximum size seen so far.
    
5. Return the maximum size.
    

I hope the steps are clear and you can properly understand the question. Now let's move toward the code.

## Solution

```java
public static int biggestNeighbourSize(List<List<Integer>> matrix) {
    int max_size = 0;
    boolean[][] visited = new boolean[matrix.size()][matrix.get(0).size()];

    // Traverse the matrix and search for houses
    for (int i = 0; i < matrix.size(); i++) {
        for (int j = 0; j < matrix.get(0).size(); j++) {
            // If the current cell is a house and is not visited
            if (matrix.get(i).get(j) == 1 && !visited[i][j]) {
                // Perform a DFS search to count the size of the house group
                int house_size = dfs(matrix, visited, i, j);

                // Update the maximum size seen so far
                max_size = Math.max(max_size, house_size);
            }
        }
    }

    return max_size;
}

private static int dfs(List<List<Integer>> matrix, boolean[][] visited, int row, int col) {
    // Check if the current cell is within the matrix bounds and is not visited
    if (row < 0 || row >= matrix.size() || col < 0 || col >= matrix.get(0).size() || visited[row][col] || matrix.get(row).get(col) == 0) {
        return 0;
    }

    // Mark the current cell as visited
    visited[row][col] = true;

    // Count the current cell as part of the house group and search its neighbours
    int count = 1;
    count += dfs(matrix, visited, row, col+1);
    count += dfs(matrix, visited, row, col-1);
    count += dfs(matrix, visited, row-1, col);
    count += dfs(matrix, visited, row+1, col);

    return count;
}
```

### Explanation of the above code

The `dfs()` function is a recursive function that performs a depth-first search to count the size of a house group starting from a given cell `(row, col)` in the matrix. It takes the matrix `matrix`, the visited array `visited`, and the row and column indices `row` and `col` of the starting cell as its arguments.

The first step of the function is to check whether the current cell is within the matrix bounds, is not visited, and is a house (i.e., has a value of 1 in the matrix). If any of these conditions is not satisfied, the function returns 0, indicating that the current cell is not part of the house group.

If the current cell is valid, the function marks it as visited in the `visited` array and counts it as part of the house group. Then, it recursively calls itself to search the four neighboring cells of the current cell: `(row, col+1)`, `(row, col-1)`, `(row-1, col)`, and `(row+1, col)`. The size of the house group is the sum of the counts returned by the four recursive calls plus 1 (for the current cell).

Finally, the `biggestNeighbourSize()` function initializes a variable `max_size` to 0, and a boolean array `visited` with the same size as the input matrix. It then iterates over all cells of the matrix, checking whether each cell is a house and has not been visited. For each unvisited house, it calls the `dfs()` function to count the size of the house group and updates the maximum size seen so far.

Finally, the function returns the maximum size of any house group found in the matrix.

### Complexity analysis⌛

This solution has a time complexity of O(nm), where n and m are the dimensions of the matrix, as it performs a DFS search for each unvisited house in the matrix. However, the worst-case time complexity can be much higher if the matrix has many disconnected house groups, as the DFS search needs to be repeated for each group. The space complexity is also O(nm), as it uses a visited array to mark visited cells.

`Thank you for reading my blog. Do share your views in the comments. I read them all and don't forget to subscribe to my newsletter to never miss an update. 😄❤️`