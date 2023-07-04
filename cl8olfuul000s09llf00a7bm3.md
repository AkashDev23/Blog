---
title: "Recursion in java for beginners part-2"
datePublished: Fri Sep 30 2022 14:41:44 GMT+0000 (Coordinated Universal Time)
cuid: cl8olfuul000s09llf00a7bm3
slug: recursion-in-java-for-beginners-part-2
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/Df7ohmyJYlE/upload/v1664544647828/bYLH1lYaT.jpeg
tags: java, best-practices, recursion, problem-solving-skills, java-beginner

---

This blog is the continuation of my previous blog and if you haven't read it yet then do check it out.

So today through this blog we'll be looking into some questions of recursion which will help us more to clear concepts easily.

# Recursion examples

### [Fibonacci number](https://leetcode.com/problems/fibonacci-number/) `(easy)`

As we discussed earlier to solve any recursion problem first we need a *Base case* and then a *Recursive case*. The code to print nth fibonacci numbers using recursion will look like this.

```plaintext
static int fibo(int n){//make a static function named fibo that will take integer as an input and will return an integer. 
//Since the first and second element is one we will put an if condition to check whether the integer entered is 1 or 2
// If the number entered is 1 or 2 then, it will simply return 1
  if(n== 1 || n == 2){ //this is the base case
    return 1; } 
//If the number is greater than 2 then it will add the 2 numbers before the number then return their sum
return fibo(n-1) + fibo(n -2); //This is the recursive case
}
//Driver function
class fibonacci{
public static void main(String [] args){
System.out.println(fibo(10) +" ");
}

//Output
//55
```

### Sum triangle from the array`(easy)`

Print a sum triangle of a given array of integers such that the first level has all array elements. From then, at each level number of elements is one less than the previous level and elements at the level is be the Sum of the consecutive two elements in the previous level.

```plaintext
//we'll make a static method that won't return anything and it will take an array of integer
    static void printTriangle(int arr[]) {
//If the length of the array is less than 1 that means no element is present in the array so it will simply return  the function. 
        if(arr.length<1){//This is the **base case** of the program
            return;
        }
//make a new array which has one less element than the previous array
        int[] temp = new int[arr.length - 1];
        {
//check for each iteration
            for (int i = 0; i < arr.length - 1; i++) {
                int x = arr[i] + arr[i + 1];//take sum of the consecutive element.
                temp[i] = x;//store these new values in the temp array that we created
            }
            printTriangle(temp);//Make a recursive call then pass the temp array
            System.out.println(Arrays.toString(arr));//print the array 
//we are printing the array at the last so that the smaller elements are printed first
        }
  public static void main(String[] args)
    {
        int[] A = { 1, 2, 3, 4, 5 };
        printTriangle(A);
    }
//output
//48 
//20, 28 
//8, 12, 16 
//3, 5, 7, 9 
//1, 2, 3, 4, 5
```

## Write a recursive function for given n and a to determine x:

### Try this on your own

```plaintext
      n = a ^ x //base case
      a = 2, 3, 4
      (2 ^ -31) <= n <= (2 ^ 31) - 1    //recursive case
```

## Check if a number is prime or not

```plaintext
static boolean isPrime(int n, int i)
    {
 
        // Base cases
        if (n <= 2)
            return (n == 2) ? true : false;//this is a shortcut for if condition it basically means check if n=2 if yes return tue else false
        if (n % i == 0)//if the remainder we are getting after dividing n bu i is zero then return false
            return false;
        if (i * i > n)//if i^2 is greater than n then return true
            return true;
      
        // Check for next divisor
        return isPrime(n, i + 1);
    }
     
    // Driver program to test above function
    public static void main(String[] args)
    {
 
        int n = 15;
 
        if (isPrime(n, 2))
            System.out.println("Yes");
        else
            System.out.println("No");
    }
}
//output
//no
```

# How to practice recursion?

To practice recursion you need to follow some steps.

1. Make a recursive tree for every problem you solve.
    
2. See the flow of the function using the debug pointer.
    
3. Identify and focus on left tree calls and right tree calls.
    

These are some of the example of recursion and few points that you can use to practice. If you still have any doubt and do comment I'll try my best to resolve your query