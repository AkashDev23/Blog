---
title: "Unleash the Power of Newton's Method - The World's Fastest Square Root Algorithm"
datePublished: Sun May 28 2023 13:54:16 GMT+0000 (Coordinated Universal Time)
cuid: cli7hf9ad000309jzec2q7bd4
slug: unleash-the-power-of-newtons-method-the-worlds-fastest-square-root-algorithm
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/MskbR8VLNrA/upload/79eb312cd9b3f2e824762e440df31c0e.jpeg
tags: development, computer-science, research, mathematics, wemakedevs

---

I've been calculating square roots of numbers for a long time now, but recently I came to know about a new method, and to my surprise, it was the fastest way to calculate the root of any number. This method was developed by none other than Sir Isaac Newton. This method is the generalized form of the **Newton-Raphson Method**. Sir Newton is known for his contributions in many fields, including *Astronomy, Chemistry, Prisms, Gravity, Calculus, the Binomial Theorem, and more.* Joseph Raphson also made a major contribution to this formula. Newton's other works are so gigantic that such massive discoveries are often overlooked.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1685260138613/aea5ae24-9322-4db0-878e-b43d394ca281.jpeg align="center")

## History of the formula

Newton's method, also known as the Newton-Raphson method, is an iterative numerical method for finding the roots of a function. <mark>It was developed by Sir Isaac Newton and Joseph Raphson in the late 17th century.</mark> The method is widely used in various fields of science, engineering, and computer science due to its effectiveness in approximating solutions. The basic idea behind Newton's method is to iteratively refine an initial guess to converge toward the root of a function. It utilizes calculus by approximating the function with its tangent line at each iteration. Now you may have a question in your mind why do I need to learn this method? I already know the traditional way. Now why this??

### Why use this method?🤔

<mark>The answer we get with the traditional method is often approximate, numerical methods prioritize the accuracy of results.</mark> Some algorithms, like Newton's method, converge toward the desired result but never reach it in a finite number of steps. The speed of convergence and the impact of rounding errors in computer arithmetic are essential considerations in achieving accurate results.

In addition to finding correct solutions, Newton's methods also focus on the time and computational resources required to compute those solutions. This is because computer science involves the practical aspect of implementing algorithms efficiently. Now let's understand the mathematics of this method.

# Mathematics behind the method

The basic idea behind Newton's method is to iteratively refine an initial guess to converge toward the root of a function. It utilizes calculus by approximating the function with its tangent line at each iteration. The process can be summarized as follows:

1. *Choose an initial guess, x₀, close to the root.*
    
2. *Calculate the function value and its derivative at x₀: f(x₀) and f'(x₀).*
    
3. *Compute the next approximation, x₁, using the formula: x₁ = x₀ - f(x₀) / f'(x₀).*
    
4. *Repeat steps 2 and 3 until the desired level of accuracy is achieved.*
    

## The generalized form of the formula

The formula **<mark>Xn+1 = 1/2(Xn + a/Xn)</mark>** is a generalized form of the Newton-Raphson method.

In this case:

* Xn represents the current approximation of the square root.
    
* a is the number for which we want to find the square root.
    

### Understand with an example

Let's take an example.

a = 16 and Xn = 24 *You can take any number I've taken 24 in this case you can take any.*

Let's see how it works.

***Iteration 1***: X1 = 1/2(24 + 16/24) = 1/2(24 + 0.6667) = 1/2(24.6667) = 12.3334

***Iteration 2***: X2 = 1/2(12.3334 + 16/12.3334) = 1/2(12.3334 + 1.2985) = 1/2(13.6319) = 6.8159

***Iteration 3***: X3 = 1/2(6.8159 + 16/6.8159) = 1/2(6.8159 + 2.3469) = 1/2(9.1628) = 4.5814

***Iteration 4***: X4 = 1/2(4.5814 + 16/4.5814) = 1/2(4.5814 + 3.4950) = 1/2(8.0764) = 4.0382

***Iteration 5***: X5 = 1/2(4.0382 + 16/4.0382) = 1/2(4.0382 + 3.9594) = 1/2(8.9976) = 4.4988

***Iteration 6***: X6 = 1/2(4.4988 + 16/4.4988) = 1/2(4.4988 + 3.5569) = 1/2(8.0557) = 4.0279

***Iteration 7***: X7 = 1/2(4.0279 + 16/4.0279) = 1/2(4.0279 + 3.9782) = 1/2(8.0061) = 4.0030

***Iteration 8***: X8 = 1/2(4.0030 + 16/4.0030) = 1/2(4.0030 + 3.9993) = 1/2(8.0023) = 4.0012

***Iteration 9***: X9 = 1/2(4.0012 + 16/4.0012) = 1/2(4.0012 + 3.9998) = 1/2(8.0010) = 4.0005

***Iteration 10***: X10 = 1/2(4.0005 + 16/4.0005) = 1/2(4.0005 + 3.9999) = 1/2(8.0004) = 4.0002

As the iterations progress, the value of Xn approaches the actual square root of 16, which is 4. Therefore, after 10 iterations, the value of X10 is a close approximation to the square root of 16.

I hope This mathematical explanation is clear to you. Now let's understand how to code it. After all, it's a tech blog and it would be better if you could also know the code.

## Code of the formula

```java
public class akashMain {

    public static double newtonSqrt(double n, double precision) {
        /*
         * This function uses Newton's method to find the square root of a number.
         * It returns the approximated square root with a desired level of precision.
         */
        double approx = n/2;  // initial guess
        while (true) {
            double betterApprox = (approx + n/approx)/2;  // calculate better approximations
            if (Math.abs(betterApprox - approx) < precision) {
                return betterApprox;  // return when desired level of precision is reached
            }
            approx = betterApprox;
        }
    }

    public static void main(String[] args) {
        double result = newtonSqrt(16, 0.00001);
        System.out.println(result); // Output: 4.000000000002
    }
}
```

This is the Java code of the above formula. And one good news for you guys I have now learned Python as well, so from now on, I will be able to provide code examples in both Java and Python.😅

```python
def newton_sqrt(n, precision):
    """
    This function uses Newton's method to find the square root of a number.
    It returns the approximated square root with a desired level of precision.
    """
    approx = n/2  # initial guess
    while True:
        better_approx = (approx + n/approx)/2  # calculate better approximations
        if abs(better_approx - approx) < precision:
            return better_approx  # return when desired level of precision is reached
        approx = better_approx

result = newton_sqrt(16, 0.00001)
print(result)  # Output: 4.000000000002
```

That's all for today. I hope you understood what the Newton Method is and how to code it. If you have any doubts, please feel free to comment. And if you found this article useful, don't forget to like and share it with your friends.

---

# Reference

If you want to know more about it you could read this [Pdf.](https://math.mit.edu/~stevenj/18.335/newton-sqrt.pdf#:~:text=Recall%20that%20Newton%E2%80%99s%20method%EF%AC%81nds%20an%20approximate%20root%20off%28x%29,forf%28x%29%20%3Dx2%20athis%20yields%20the%20Babylonian%20formula%20above.)

![](https://media.giphy.com/media/uWlpPGquhGZNFzY90z/giphy.gif align="center")

Thanks for reading.❤