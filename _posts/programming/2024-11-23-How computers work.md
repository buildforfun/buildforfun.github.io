---
layout: post
title:  "How computers work"
categories: [ programming]
date:   2024-11-23 11:00:00
---

How computers work
----
Computers were invented by Charles Babbage. He made an analytical engine:
- hardware - physical parts
- software - instructions: holes and pins

Ada lovelace then recognised how this could be used with different logic. Made up of binary digits - 0s and 1s. think of it like atoms of computing. Each one or zero is a binargy digit or bit.  The bits are used to create logic gates (AND, OR). Algorithmns are just a set of instructions to get from A to B.

Hardware
----
The CPU or Central Processing Unit is like the brain of the computer. It takes instructions from programs (like games or apps) and tells the other parts what to do. The CPU (central processing unit) fetches these binary instructions and data from memory, decodes them, and performs the specified operations in its arithmetic logic unit (ALU).
- Cores and Threads: More cores and threads allow for better multitasking and performance in demanding applications.
- Clock Speed: Measured in GHz, higher speeds mean faster processing.

The RAM or Random Access Memory is like a helper for the CPU. It holds information that the CPU needs to work with right away, kind of like short term memory.
The hard drive or SSD is where all your files, games, pictures, and videos are kept when you're not using them. It's like the long term memory that the CPU can access when it needs something.

The motherboard is like the main road that connects all these parts together. It has slots where you can plug in the CPU, RAM, and other components. Your computer also needs input devices like a keyboard and mouse so you can tell it what to do. And it needs output devices like a monitor to display everything, and speakers to play sounds.

All these parts work together when you want to do something, you give instructions through the keyboard and mouse (input). The CPU gets those instructions and fetches what it needs from storage and RAM. It does all the calculations and then sends the output, like graphics and sound, to the monitor and speakers.

Transistors
----
At the most basic level, computers are made up of millions of tiny electronic components called transistors. A transistor acts as an electronic switch that can be either on or off, allowing or blocking the flow of electrons (electrical current). The on state of a transistor is represented by the binary digit 1, while the off state is represented by 0. This on/off, 1/0 state is called a bit (binary digit), which is the smallest unit of data in computing. By combining multiple bits together in specific patterns, computers can represent more complex values and data types. 

All this data in binary form is stored and processed by the computer's circuits and memory chips, which are made up of billions of transistors switching on and off to represent 1s and 0s.

Software
----
1. **Numbers**: In the binary number system, each position in a number has a value double the position to its right. For example, the binary number 1011 represents (1x2^3) + (0x2^2) + (1x2^1) + (1x2^0) = 8 + 0 + 2 + 1 = 11 in decimal.
2. **Text**: Characters like letters and symbols are assigned unique numerical values based on encoding schemes like ASCII or Unicode. These numerical values are then represented in binary. For example, the letter 'A' is 65 in decimal, which is 01000001 in binary.
3. **Images**: Digital images are made up of pixels, each pixel being a combination of red, green, and blue color values. These color values are represented as binary numbers that the computer can process and display.

Writing programms in 1,0s isn't really realistic.
0. Binary 
1. Assembly language - e.g. add -> assembler translate add to 1, 0s
2. High level languages - C, C++
