---
title: "Bubble sort in java"
datePublished: Tue Nov 01 2022 16:56:34 GMT+0000 (Coordinated Universal Time)
cuid: cl9ygciow000c09l00r742ym9
slug: bubble-sort-in-java
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/BRkikoNP0KQ/upload/v1667971315676/dn-_dVvcZ.jpeg
tags: algorithms, java, beginners, recursion, bubble-sort

---

**Bubble sort** is the simplest sorting algorithm. It is an algorithm that in every step compares the adjacent elements and swaps them if they are in wrong order. This algorithm is also known as Sinking sort and Exchange sort algorithm. We can use this algorithm to sort both arrays and linkedlist but in this blog post I'll be talking only about arrays. 
## Difference between various sorting algorithms. 
In every sorting algorithm we are going to do something at each pass. We will try to solve the algorithm step by step. You will think that if we are doing the same thing in all the algorithms that what is the difference between them. So the main difference between all these algorithms is what they are doing in each pass/step. 
## How bubble sort works?

- We will use a nested for loops using variables i that will run from 0 to (n-1) and j will run from 0 to (n-i) where n is the length of the array. 
- Here i is used as a counter and j is sorting the array step by step and it will do it (n-1) times. 
- If the element at j is smaller than the element at (j-1) then swap these elements, else increment j. 
- Return the sorted array.

###  Example
In the following example, I have taken an array of size 4 which is [ 7, 6, 4, 3 ].

![0_lq-ZpDYjvYGmS7PO.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1667156449223/BIyTH_XMI.png align="left")
*** First pass***
With the first pass through the array, the largest element will come at the end. In the above example i will point to arr[0] and j will point to arr[1]. Now check If arr[j]<arr[j-1] then swap and increment j. 7 and 6 is swapped. Now again check the same thing where arr[j]= arr[j+1]. Now, 7 and 4 is swapped. This process will be continued untill the largest element i.e. 7 in this case is at the last index of the array. 

*** Second pass***
Now again all the steps of the first pass will be repeated. Only the values will be changed. 

*** Third pass***
We can see here that the last 2 elements has already reached their correct index. Now the algorithm will swap 4 and 3. Then the loop will run one more time to see if their any element left for swapping or not. If no element is left then the array will be returned. 

Here we can see one thing that it does not makes sense to compare the elements that is already been sorted. After every pass the largest elements comes at the end i.e. their correct index, Hence we don't need to compare them. So, we will just check till n-i. This is the only reason why j is not running till end of the array. 

## Space and Time Complexity
### Space Complexity
Space complexity basically means how much space a particular algorithm will take. Since this algorithm is not taking any extra space like copying the array, etc. the space complexity is O(1) i.e. constant. 
That's why these algorithms are also called ***inplace sorting algorithms***. 
### Time Complexity
Time complexity for this algorithm is the maximum number of comparisons made. It basically shows how the time grows as input grows. 

***Best Case Time Complexity:*** *O(N)* The best case occurs when j never swaps for a value of i this means an array is already sorted. Hence, end the program. 

It actually takes (N-1) time. But in time complexity, we ignore the constants since we only require the mathematical function and we don't need the value. 

***Worst Case Time Complexity:*** *O(N^2)* The worst case occurs when an array is reverse sorted.

In the worst case, the total number of iterations or passes required to sort a given array is (N-1). where ‘N’ is a number of elements present in the array.

### For worst case

*Number of swaps = Number of comparisons*                                                                                                       
Total comparisons= (n-1) + (n-2) +  (n-3) + . . . 2 + 1                                                                                                                   
                              = (n-1)*(n-1+1)/2  { by using sum of n natural Number formula }                                                          
                              = n (n-1)/2        

Constants are not considered and less dominant terms are ignored. 
## Stable sorting algorithm
A sorting algorithm is said to be stable when the original order is maintained for values that are equal in the sorted output. 

Check out this example for better understanding stable and unstable algorithms. 

![stability-sorting.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1667319983684/F0wSQXE-7.jpg align="left")
In the original array of balls, the green 10 was before the orange 10 and in the sorted one, this order is maintained. Same is the case for all the other numbers. 

## Code for bubble sort
Usually in the documentations the code is provided below the explanation but here the case is opposite. Because I feel that It's important to first understand the concept of the algorithm before jumping into the code. 
### Iterative approach
*I have used java language to write the code.*

```
static void bubbleSort(int[] arr){
//run the steps (n-1) times
  for(int i=0; i<arr.length; i++){
//for each pass max item will come at the last respective index
//j can also run till the length of arrary but it is running till array.length-i because it makes no sense to check the sorted items. 
    for(int j=1; j<arr.length-i; j++){
//swap items if it is smaller than the previous one
      if(arr[j]<arr[j-1];
      int temp=arr[j];
      arr[j]=arr[j-1];
      arr[j-1]=temp;
      }
  }
}

``` 
### Recursive approach

```
public static void bubbleSort(int arr[], int n){
  if(n==0 || n==1){
return;
}
for(int i=0; i<n-1; i++){
     // if arr[i] greater than arr[i+1] then
            // swap(arr[i], arr[i+1])
            if (arr[i] > arr[i + 1]) {
                swap(arr, i, i + 1);
            }
        }
        bubblesort(arr, n - 1);
    }
 
    // function to swap element of arr present at index i &
    // j
    public static void swap(int[] arr, int i, int j)
    {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
``` 
If you have read this far and understood bubblesort through this article then do share it on your socials. If you still have any doubts you can comment below this blog post. thanks.. ❤️