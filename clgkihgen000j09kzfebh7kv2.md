---
title: "How to Install Emu8086 in windows and Write Your First Hello World Code"
datePublished: Mon Apr 17 2023 07:25:34 GMT+0000 (Coordinated Universal Time)
cuid: clgkihgen000j09kzfebh7kv2
slug: how-to-install-emu8086-in-windows-and-write-your-first-hello-world-code
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/FO7JIlwjOtU/upload/488c2ce8f880d82c3290708d3a91d1da.jpeg
tags: programming-blogs, coding, system-architecture, hardware, assembly

---

Welcome, readers! 🎉 In this blog post, I'm happy to share with you all about the emu8086 software installation process, and how you can easily create your very first "Hello World" program. Whether you're a beginner or a seasoned programmer, this step-by-step guide will show you how to get started with emu8086. 💻 So, without further ado, let's start! 🚀

# Introduction

Before getting over to install it, let's first have a brief overview of assembly language. 🤔

Assembly language is a programming language that operates at a low level and is utilized to create software that interfaces directly with computer hardware. 🖥️ Unlike high-level programming languages like Python or Java, writing code in assembly requires a thorough comprehension of computer architecture, as it entails composing instructions in binary code that the computer can interpret. 💻

Understanding assembly language is paramount because it allows us to grasp how programs interface with the OS, processor, and BIOS. It also provides insight into how data is represented in memory and other external devices, how the processor accesses and executes information, how instructions access and manipulate data, and how programs interface with external devices. 🔍💡

EMU8086 allows users to emulate outdated processors that were once prevalent in Mac and Windows computers during the 1980s and early 1990s. 🕹️

# How to install EMU8086

## System requirements

As this software is quite dated, you need not fret over its system requirements; it should function on most basic laptops. Nevertheless, the following are the system requirements for your information.

* Intel Pentium III or higher processor
    
* 256 MB of RAM
    
* 50 MB of free hard disk space
    
* Windows 2000/XP/Vista/7/8/10
    

One thing to note is this software is a 32-bit application, so it may not run properly on 64-bit operating systems without using an emulator or virtual machine.

## Downloading and installing Emu8086

1. 🖥️ To get started, open your preferred web browser and search for EMU8086, or simply click on [this link](https://emu8086-microprocessor-emulator.en.softonic.com/?ex=DINS-635.3).
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681667928291/ab195dce-8e35-494d-923d-0a5a494cec06.png align="center")

1. 🖱️ Upon clicking the link, you will be directed to a webpage resembling the one shown above. From there, click the "Download for Windows" button to begin the download process.
    

1. 📩 After clicking the download button, a dialog box will appear. Click "No thanks, I will continue downloading EMU8086 - MICROPROCESSOR EMULATOR" to proceed with the download.
    
2. 📥 Your download will begin automatically, and the zip file containing the software will be saved in your downloads folder. Look for a file with a similar name to the one shown below.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1681668233322/a64f3909-f07d-4d60-89fa-c60d8a62a2fd.png align="center")

You could see a zip file or something like this in your downloads section.

1. 🔓 Once the download is complete, right-click on the zip file and select "Extract All" to extract the contents to a location of your choosing.
    
2. 📂 Upon extracting the files, navigate to the extracted folder, where you will find two files: "setup" and "Readme." Double-click on the "setup" file to begin the installation process.
    
3. 🔍 Follow the installation prompts by clicking "Next" each time until you see the "Install" button. Click "Install" to finalize the installation process.
    
4. 🎉 Congratulations, the software is now installed on your system!
    

# Writing Your First Hello World Code

To launch the EMU8086 software on your system, simply locate its icon and double-click on it, as shown below.

![](https://img.apponic.com/28/3/ca609bab1385855220fd15dff809b2f0.png align="center")

1. 1. After opening the EMU8086 software, click on the "New" button, followed by the "Ok" button to confirm. This will bring up a blank screen where you can begin writing your code.
        

```apache
; Set the origin point to 100h
org 100h

; Define a variable 'msg' with the string "Hello world $" and store its memory location in 'da'
msg db "Hello world $"
mov da, offset msg

; Load the value 9 into the 'ah' register to indicate that we want to print a string to the console
mov ah, 9

; Call interrupt 21h, which will print the string stored at the memory location specified by the 'da' register
int 21h

; Return control back to the operating system
ret
;Code by Akash Dev
```

## Explanation

1. `org 100h`: This sets the origin of the program to memory address 100h. This is a common practice in Assembly language programming as it helps to organize and manage the program's memory usage.
    
2. `mov da, offset msg`: This moves the offset of the message "Hello world" into the `da` (Data Address) register. This sets the starting memory address of the message in memory.
    
3. `mov ah, 9`: This moves the value 9 into the `ah` (Auxiliary) register. In DOS (Disk Operating System), the value 9 in the `ah` register is used to display a string on the console screen.
    
4. `int 21h`: This is an interrupt instruction that tells the computer to execute the function specified by the value in the `ah` register. In this case, it triggers the DOS interrupt 21h which displays the message "Hello world" on the console screen.
    
5. `ret`: This is a return instruction that tells the program to return to the calling function. In this case, it tells the computer to return to the operating system after executing the `int 21h` instruction.
    
6. `msg db "Hello world $"`: This defines the message "Hello world" and stores it in the program's data section. The `$` character represents the end of the string and is used to terminate it. The `db` directive tells the assembler that the following characters should be treated as data bytes.
    

*If you found this helpful, please leave a comment and consider subscribing to my newsletter! 😊*