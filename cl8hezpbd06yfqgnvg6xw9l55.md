---
title: "Strings in java explained"
datePublished: Sun Sep 25 2022 14:06:50 GMT+0000 (Coordinated Universal Time)
cuid: cl8hezpbd06yfqgnvg6xw9l55
slug: strings-in-java-explained
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/hTeYcjviZ-s/upload/v1664094911235/Ap3XuyTNq.jpeg
tags: java, beginner, string, strings, java-beginner

---

# What are Strings?

String is a data type in Java which is a sequence of characters. In simple words we can understand this as an array of characters.  
## In Java we can implement string in two ways

1. By string literal
2. By new keyword

### - By String literal String is created in the following way. 

```
String name = "Akash dev";
```

In the above code snippet the term **String** is a data type, the term **name** is a reference variable and **Akash dev** is the String object respectively. 

If we are creating more than one String literal of the same object then all the literals will point to the same object. 

```
String a="Akash";  
String b="Akash";
``` 

In the above case String b doesn't create a new instance. Since both the strings have same value and both the ref. variable i.e. a and b will point to the same object.
 
Java does this to make it more memory efficient.                                                                                 
#### When we run
```
System.out.println(a==b);
//it will give output as true.
``` 
> #### How this is working internally
You may have a question in your mind that if both the variables are pointing to the same object then changing value of any one string will result in change of the value of other string also??
So, the simple answer of this question is **NO**. 

Now, you may wonder that what is happeining here. Both are pointing to same object but changing one isn't changing the other. It's so confusing... 
Wait! Let me make it clear.. 
To understand this properly first you need to understand where the strings are created.
### Where are the Strings created?
The reference variable of the String a & String b in the above case are created in the *Stack *memory of the system. I'll explain stack in my other blogs till then just understand that  
> Stack is a linear data structure that works on the "LIFO"*(last in first out)* principle. For eg. Notebooks stacked on a teacher's table. The notebook that is kept at last will be picked first and vice versa.

The String variable that is declared at last is called at first and so on.

The value of the String i.e. ``` Akash ``` 
in this case is stored in the *heap* memory. in heap memory there's a **String pool** which contains all the String objects. If JVM find the string with the same value in the pool, it will not create a new object but will return the reference to the same instance.


Ok, so now I have understood that Strings are created in heap memory but I haven't got my answer yet. Why changing value of one String doesn't affect the value of other?

The answer to your queston is **Immutability**. Yes, you read it correct Strings in Java are immutable in nature i.e. they can't be modified or changed once created. 
### Why Strings are immutable in Java?
The String is immutable in Java because of the security, synchronization and concurrency, caching, and class loading. Let me explain it to you in a simplified way
> Suppose the fav food of 5 people named Hari, Akash, Ram, Amit and Aditya is same i.e. **Dosa**. This data is stored in a String in the following way

```
String hariFavFood  ="Dosa";
String akashFavFood ="Dosa";
String ramFavFood   ="Dosa";
String amitFavFood  ="Dosa";
String adityaFavFood="Dosa";
``` 
> Now suppose Amit goes to Itly and tastes pizza and now he says that his fav food is pizza. If strings won't have been immutable then changing the value of Amit's food would also change the fav food of rest of the guys. Which I don't think they would prefer. 

To avoid situations like these strings in java are immutable.

Now a question may arise in your mind that what if I don't care about what Java does and what is the property of strings. I want to create different objects of the same value.                 
Is it possible to do so?

The answer is **Yes**. Yes you can create different objects of the same value and to perform this task you need to use **new** keyword.

### - By new keyword String is created in the following way. 


```
String i = new String("Akash");
String j = new String("Akash");
``` 
In this case both the String i & String j are pointing to different String object. These values are created outside the pool in heap memory.                                                                                            
#### When we run
```
System.out.println(i==j);
//it will give output as false.

``` 
> But why is it giving false? I can literally see with my eyes that both Akash & Akash is completly same then why is it giving false as answer. It's confusing me now.

When we use (==) operator the java compares the value of the variables basically it checks whether the variables are pointing to same object or different. If both variables are pointing to the same object then the output will be true else it will give false. 
#### Check only the value of the string

When we only need to check the value of the String we will use ```.equals()``` method.
```
System.out.println(i.equals(j)
//This will give the output as true in this case.
```
The ```.equals()``` method compares the value of the Strings and returns *true* if the value is same else it will return *false*.

Many useful methods are provided by *java.lang.String* that can be used to perform operations on Strings..

