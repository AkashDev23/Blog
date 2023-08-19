---
title: "5 step approach for problem solving"
datePublished: Sat Aug 19 2023 08:16:27 GMT+0000 (Coordinated Universal Time)
cuid: cllhqwj69000109mias2jey1c
slug: 5-step-approach-for-problem-solving
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/_UeY8aTI6d0/upload/5a7f9b4affdcc0ac5be2f051989ec8b0.jpeg
tags: interview, algorithms, tips, problem-solving, problem-solving-skills

---

While learning computer science, we usually **grasp the theory of algorithms**, but often, *theoretical knowledge isn't sufficient*. While it's essential to have a deep understanding of the concepts, it's not enough. When we're in an interview, and the interviewer asks us to develop a program, we can't just simply explain the theory. At that time, we need to **comprehend the question and also code the solution for it**. In this blog, I'll be sharing a **5-step approach to problem-solving**.

The five steps are:

1. **Constraints**
    
2. **Idea Generation**
    
3. **Complexities**
    
4. **Coding**
    
5. **Testing**
    

I've just introduced you to the steps. If you'd like a detailed explanation of these steps, please continue reading.

## Constraints🔎

When solving any problem in an interview, many people make assumptions and start working based on those assumptions. **You should ask clarifying questions to your interviewer**. Many times, there is a lot of missing data that you need to collect from your interviewer before beginning to solve a problem.

In this step, you will capture all the constraints of the problem. We should never try to solve a problem that is not completely defined. In an interview, the interviewer expects you to ask questions to clarify the problem.

Not understanding what I'm trying to convey? Let me explain by giving you a few examples.

Suppose your interviewer asks you to write an algorithm to sort numbers:

1. The first thing you need to ask is what kind of data is provided. Suppose the interviewer responds with integers.
    
2. The second thing you need to know is the size of the data. You will use a different algorithm if the data size is 10 integers or 1 billion integers.
    

Now you should have a better understanding of what a constraint is. Let me provide you with some possible questions that you can ask in different scenarios.

**Constraints for an Array:**

1. What's the size of the array?
    
2. What is the range of values in each element? What is the minimum and maximum value?
    
3. What is the type of data in each element? Is it an integer or a floating-point number?
    
4. Does the array contain unique data, or are there duplicates?
    
5. What's the length of each string? What is the minimum and maximum length? (If a string array is given)
    

**Constraints for a Graph:**

1. How many nodes are there in the graph?
    
2. How many edges are there in the graph?
    
3. Is it a weighted graph? What is the range of weights?
    
4. Is the graph directed or undirected?
    
5. Is there a loop in the graph?
    
6. Is there a negative sum loop in the graph?
    
7. Does the graph have self-loops?
    

## Idea Generation💡

There are a lot of problems, and new questions are created every day. Therefore, it's important to know how to handle new problems. Even if you know the solution to a particular problem, *you still need to discuss it with the interviewer and try to reach the solution*. Many times, the interviewer modifies a question, so the approach to solving it will vary.

Now arises a question: if new problems are created every day, then how can we solve them? The answer is quite simple. **You need to do a lot of practice**, and the more you practice, the higher your chances of solving any unseen question. When you've solved enough problems, you'll be able to **spot patterns in the questions** and solve new problems more easily.

A strategy that you can use to solve a new problem:

1. **Try to simplify the task** (divide the problem into simpler known sub-problems)
    
2. **Try a few examples** (Run the code by taking small examples)
    
3. **Think of a suitable data structure**
    
4. **Think about similar problems that you have already solved**
    

## Complexities🤔

Solving a problem isn't just about finding the correct solution; it's more about finding the **optimal solution**. If your solution isn't efficient in terms of speed and memory management, then you should reconsider your approach. You need to perform a **Big-O analysis**. If you believe your solution is suboptimal and there might be a better solution, then you should strive to discover it.

Most interviewers expect you to be able to determine the **time and space complexities** of the algorithms you write. In certain problems, there are trade-offs between space and time complexities; in such cases, you need to understand those trade-offs as well. Sometimes, using slightly more space can greatly improve the efficiency of an algorithm.

For example, *Quick sort and merge sort* both have an average-case time complexity of O(n log n), but Quick sort's worst case is O(n^2), whereas Merge sort requires O(n) extra space to solve the algorithm. **Understanding these trade-offs beforehand is crucial**.

## Coding✏️

Up to this point, you have identified all the constraints of the problem, proposed potential solutions, and evaluated the complexities of those solutions, and the interviewer seems impressed with your approach. Now, it's time to write the final code.

We are accustomed to coding in an IDE like VS Code. However, many people struggle when asked to write code on a whiteboard or paper. Therefore, we should practice writing code by hand a little. **Thinking before writing every word is essential**, as there are no back buttons or red lines to guide you in case of mistakes. Aim to write modular code. Create small functions to keep the code clean and well-organized. If there's a swap function available, use it and inform the interviewer that you will provide the implementation later. It's a common understanding that you can write a swap function, right? Or perhaps you can't? 🤔

## Testing🧪

And now, we arrive at the most crucial part. Even though you may feel like you're done once the code is written, the truth is, you're not. **Testing your code with various small test cases is of utmost importance**. Doing so not only demonstrates to your interviewer that you value testing but also instills confidence that your code isn't prone to bugs. After coding, meticulously review each line to ensure that your code is functioning as intended.

Here are some test case categories for my readers:

* **Normal test cases**: These are positive test cases, covering the most common scenarios.
    
* **Edge cases**: These represent the boundaries of your code, where it's most likely to encounter issues.
    
* **Load testing**: Put your code through its paces with substantial data. This helps determine whether your code is sluggish or memory-intensive.
    

## Conclusion⭐

In the world of computer science and programming, mastering the art of problem-solving is as essential as understanding algorithms and concepts. A successful problem solver not only possesses theoretical knowledge but also the ability to dissect problems, devise effective strategies, analyze complexities, and implement solutions. This 5-step approach we've explored—comprising Constraints, Idea Generation, Complexities, Coding, and Testing—provides a comprehensive guide to tackling problems effectively during interviews and beyond.

By following these steps, you can develop a structured problem-solving methodology that not only impresses interviewers but also strengthens your programming skills. Remember, practice is key; solving diverse problems using this approach will hone your problem-solving prowess and enhance your coding journey.

## Ready to Enhance Your Problem-Solving Skills?
![YES](https://media.giphy.com/media/2RGhmKXcl0ViM/giphy.gif)

Start your journey to becoming a confident problem solver by putting the 5-step approach into practice. Don't stop at theory—embrace real-world coding challenges and refine your abilities. Subscribe to our newsletter to receive regular updates on coding techniques, problem-solving strategies, and more! Stay ahead in the coding game and unlock your full potential.

[Subscribe to Our Newsletter](https://coolcoderr.hashnode.dev/newsletter) and embark on a journey of mastering problem-solving in the world of programming!