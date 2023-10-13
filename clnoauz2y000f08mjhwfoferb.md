---
title: "Demystifying Java Threads for Beginners"
datePublished: Fri Oct 13 2023 07:41:09 GMT+0000 (Coordinated Universal Time)
cuid: clnoauz2y000f08mjhwfoferb
slug: demystifying-java-threads-for-beginners
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/K6cC1D-_k_g/upload/ad7090d8f88d6d331a9f659547eeca32.jpeg
tags: java, learning, beginners, java-programming, threads

---

Today, as I was reading about multi-threading and threads in Java, I came across numerous resources on the internet, which left me feeling overwhelmed. Therefore, I decided to write an article on the topic. This article is intended for beginners who have no prior knowledge of the subject. So, without any further ado, let's get started.

## **Understanding Threads in Java**

A *thread* is a unit of control that performs a specific task. A thread is considered a lightweight process because it doesn't burden the CPU by demanding new resources when a new thread is created. Instead, it shares the resources of its parent thread. In contrast, a process always places a burden on the CPU by demanding new resources when a new process is created. To handle threads, Java provides the `Thread` class in the `java.lang` package.

* A thread with a lowercase "t" refers to a separate, independent path of execution in the virtual machine.
    
* A thread with an uppercase "T" is an instance of the `java.lang.Thread` class.
    
* There is a one-to-one relationship between threads executing in the virtual machine, and these threads are objects constructed by the virtual machine.
    

To start a thread, you can follow these steps:

```java
Thread t = new Thread();
t.start();
```

## **Creating Threads in Java**

In Java, threads can be created in two ways: by extending the `Thread` class or by implementing the `Runnable` interface.

1. **By Extending Thread Class:**
    
    ```java
    class NumThread extends Thread {
        // Override the `run()` method to define the thread's job.
    }
    ```
    
2. **By Implementing Runnable Interface:**
    
    ```java
    class NumThread implements Runnable {
        // Override the `run()` method to define the thread's job.
    }
    ```
    

## **Steps for Creating a Thread**

1. Create a class by extending the `Thread` class.
    
2. Override the `run()` method defined in the `Thread` class. The `run()` method is considered the heart of the thread since it defines the thread's job.
    
3. Create an object for the newly created thread.
    
4. Start the thread using the `start()` method present in the `Thread` class.
    
    Example:
    
    ```java
    class NumThread extends Thread {
        public void run() {
            // Define the job of the thread here.
        }
    }
    
    NumThread T1 = new NumThread();
    T1.start();
    ```
    

## **Thread Methods**

* `void start()`: Used to start a thread.
    
* `void stop()`: Used to stop a thread.
    
* `void run()`: Used to specify the job of the thread.
    
* `void sleep(int milliseconds)`: Used to suspend the thread for a specified time.
    
* `void suspend()`: Used to suspend a thread indefinitely until the thread uses `resume()` method.
    
* `void resume()`: Used to resume a suspended thread.
    
* `void wait()`: Used to suspend a thread until another thread notifies it using `notify()`.
    
* `void notify()`: Used to notify a waiting thread.
    

## **Thread Exceptions**

* `IllegalThreadStateException`: Occurs when a thread is moved to an invalid state.
    
* `InterruptedException`: Occurs when a thread is interrupted.
    

## **Thread Priority**

Priority is an integer value associated with each thread, specifying the thread's priority. Threads generally have three priorities defined as constants in the `Thread` class:

* `MIN_PRIORITY` (1)
    
* `NORM_PRIORITY` (5)
    
* `MAX_PRIORITY` (10)
    

You can get and set the priority of a thread using the following methods:

* `int getPriority()`: Gets the priority of the thread.
    
* `void setPriority(int priority)`: Sets the priority for the thread.
    

For example:

```java
T1.setPriority(Thread.MAX_PRIORITY);
```

## **Conclusion**

Java threads are a powerful concept for concurrent programming. They allow you to perform multiple tasks simultaneously, making your applications more efficient. Whether you choose to extend the `Thread` class or implement the `Runnable` interface, mastering threads is essential for any Java developer.

## **Subscribe to Our Newsletter**

If you found this article helpful and want to stay updated on more on this type of content and programming tips, subscribe to our newsletter. Don't miss out on valuable insights and tutorials. Happy coding!

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1697038535002/b8b1b5cb-c9cf-4ca2-9c0a-9e4cad74009d.gif align="center")