---
title: "Web development 101"
datePublished: Mon Jan 30 2023 08:16:39 GMT+0000 (Coordinated Universal Time)
cuid: cldijeju402d9xfnva8imanfk
slug: web-development-101
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/webyw4NsFPg/upload/cf738010d49b436ea99daef955a2bc2c.jpeg
tags: css, development, web-development, html5, wemakedevs

---

## Introduction

Web development is the process of building and maintaining websites. It's a combination of several different technologies and skills used to create interactive and dynamic websites.

To get started with web development, you'll need a few tools such as a text editor📝, a web browser🔎 and something to run the websites on a local server.

* Some of the popular text editors are VScode, Atom, sublime text editor, etc.
    
* You can use any modern web browser such as Chrome or Mozilla Firefox for debugging.
    
* Setting up a local server can be done by using XAMPP or MAMP.
    

## Technologies used

There are many technologies used in creating a website but in this blog, we will be talking about 3 main technologies **HTML, CSS and JavaScript.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674632328053/6990f0b1-4458-4acb-94e5-67b16501b686.gif align="center")

## 🚩HTML

### What is HTML?🤔

HTML(Hypertext Markup Language) is the foundation of every webpage and is used to define the structure and content of a webpage. It is basically the skeleton of a webpage.🩻

The basic structure of an HTML document includes the doctype declaration, head, and body tags. If we want to make a beautiful and simple website we need to use some more tags such as headings, paragraphs, lists, and images. Using these to create the webpage will help understand the concepts of nesting and attributes.

### Example:

Open any text editor to write the HTML code and save it as .html extension. You can open the file in your web browser to see the result.

Below is an example of the basic HTML page:

```xml
<!DOCTYPE html>
<html>
<head>
  <title>My first HTML page</title>
</head>
<body>
  <h1>Welcome to my website</h1>
  <p>This is my first webpage.</p>
  <img src="dog.jpg" alt="A picture of a dog">
  <a href="https://www.example.com">Learn more</a>
<footer>
    <p>Copyright ©2023 Akash's website</p>
  </footer>
</body>
</html>
```

1. The `<!DOCTYPE>` declaration in this example specifies the version of HTML being used. The `<html>` element is the container for all other HTML elements on the page.
    
2. The &lt;head&gt; element contains information about the document, such as the title that appears in the browser's title bar or tab.
    
3. The `<body>` element contains the main content of the page.
    

* In the body, there is an `<h1>` element, which is used to create a heading.
    
* `<p>` element is used to create a paragraph.
    
* `<img>` element is used to embed an image and `<a>` element is used to create a hyperlink.
    

## 🚩CSS

CSS(Cascading Style Sheets) is used to control the layout and visual presentation of web pages and is used to apply styles to HTML elements such as color, font, and spacing. CSS makes your website look beautiful and acts as magic. Mastering CSS is very difficult but with a little bit of practice, you could get used to it. 💗

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674632544625/8a61ad26-1a23-4ce8-b414-c224e270a19f.gif align="center")

#### Types of CSS

There are 3 types of CSS:

1. **Inline CS**: CSS specified within the HTML tag using the `<style>` attribute.
    
2. **Internal or Embedded CSS**: CSS embedded within the HTML file.
    
3. **External CSS**: CSS property written in a separate file with .css extension.
    

### Example:

```css
body {
      background-color: #f2f2f2;
      font-family: Arial, sans-serif;
    }
h1 {
      text-align: center;
      color: #4CAF50;
    }
p {
      font-size: 18px;
      line-height: 1.5;
      margin: 20px 0;
    }
 img {
      display: block;
      margin: 20px auto;
      width: 50%;
    }
a {
      color: #0000ff;
      text-decoration: none;
    }
```

The `body` element is set to have a background color of #f2f2f2 and use the Arial font. The `h1` element is set to be centered and have a color of #4CAF50. The `p` element is set to have a font size of 18px, a line height of 1.5, and a margin of 20px on the top and bottom.

The `img` element is set to be displayed as a block element, be centered, have a width of 50%, and a margin of 20px on the top and bottom. The `a` element is set to have a blue color and no text decoration.

## 🚩JavaScript

JavaScript is a programming language that is used to make webpage interactive and dynamic. It is also used to create things such as image sliders, form validation, and interactive maps. You can do many things if you know js, Js can be used for both frontend and backend so it becomes very necessary to have basic knowledge of js.

### Example:

```javascript
let image = document.getElementById("image");
    image.addEventListener("click", function(){
      alert("You clicked on the image!");
    });
```

The above code is using the `getElementById()` method to access the `img` element by its id attribute and `addEventListener()` method is used to attach an event listener to the image that listens for a click event. When the image is clicked, the anonymous function passed to the `addEventListener()` method will execute, which is an alert box that says "You clicked on the image!"

## 🚩What to do next?

🧑‍💻Once you have learned the basics of HTML, CSS and JS you should practice making **Responsive websites**. These are the web pages that work well on different screen sizes and devices.

🧑‍💻Learn how to **debug** your code. Debugging is the process of identifying and fixing errors in your code.

🧑‍💻Use **version control**. It is a way to keep track of changes to your code, collaborate with others, and roll back to previous versions if necessary.

### Summary😄

Web development is a very big sea🌊 and no matter how much you know it's never enough. Don't get demotivated by this line you can still be the master of this skill. The only thing you need to do is practice. The more you practice, the more you learn. There are many other topics and technologies that you can explore after mastering the basics. But, these are the foundational building blocks that you need to understand before diving into more complex topics.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674633341833/704087be-efb2-4957-8ebc-b252ce02790a.gif align="center")

Resources such as tutorials, documentation, and forums can be found online to learn more about development.

*And don't forget to build your portfolio of the projects you made. This will help you to showcase your skills and get hired.*

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1674633503060/4256da4d-cef2-4471-9fd9-3f68c3f48948.gif align="center")

Follow the step-by-step instructions provided in the blog to kickstart your web development journey and **Create your first webpage today!💥**

*Read it till the end and learned something new?*🧐

*Don't forget to* ***subscribe to my newsletter*** *so you could never miss my blogs.*😄