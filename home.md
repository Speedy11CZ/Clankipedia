---
title: Home
description: 
published: true
date: 2023-03-27T23:38:13.246Z
tags: 
editor: markdown
dateCreated: 2023-03-27T22:34:10.528Z
---

# Getting Started

Welcome to the PlayStation 2 and PlayStation 3 reverse engineering wiki. Here you will find topics such as networking and modding.

# Reverse Engineering

> Reverse engineering (also known as backwards engineering or back engineering) is a process or method through which one attempts to understand through deductive reasoning how a previously made device, process, system, or piece of software accomplishes a task with very little (if any) insight into exactly how it does so.  
> [(from Wikipedia)](https://en.wikipedia.org/wiki/Reverse_engineering)

Using reverse engineering, we are able to figure out how the game works. This is one of the first steps of modding. Since modding depends on modifying the game, the first thing we need to know is how the game works. But it's not easy. Reverse engineering requires an understanding of the code (which is in Assembler, but various tools allow converting Assembler code into more readable pseudocode) and a lot of patience. In addition, modding a game can sometimes result in the game crashing if the mod is improperly written.

## Tools for Reverse Engineering

### [Ghidra](https://ghidra-sre.org/)

![Ghidra](https://upload.wikimedia.org/wikipedia/commons/7/77/Ghidra-disassembly%2CMarch_2019.png)

---

> Ghidra is a free and open source reverse engineering tool developed by the National Security Agency (NSA) of the United States. The binaries were released at RSA Conference in March 2019; the sources were published one month later on GitHub. Ghidra is seen by many security researchers as a competitor to IDA Pro. The software is written in Java using the Swing framework for the GUI. The decompiler component is written in C++. Ghidra plugins can be developed in Java or in Python (provided via Jython).  
> [(from Wikipedia)](https://en.wikipedia.org/wiki/Ghidra)

Ghidra is an open-source reverse engineering tool released by the NSA. The tool can be downloaded for free.  

### [Interactive Disassembler (IDA)](https://hex-rays.com/ida-pro/)

![IDA](https://do1alx.de/wp-content/uploads/2022/01/headline-850x457.png)

---

> The Interactive Disassembler (IDA) is a disassembler for computer software which generates assembly language source code from machine-executable code. It supports a variety of executable formats for different processors and operating systems. It also can be used as a debugger for Windows PE, Mac OS X Mach-O, and Linux ELF executables. A decompiler plug-in for programs compiled with a C/C++ compiler is available at extra cost. The latest full version of IDA Pro is commercial, while an earlier and less capable version is available for download free of charge (version 7.6 as of March 2021).  
> [(from Wikipedia)](https://en.wikipedia.org/wiki/Interactive_Disassembler)

IDA is a commercial reverse engineering tool used by large security companies. Unlike Ghidra, IDA is a paid tool. There is a free version, but it is insufficient for reverse engineering PlayStation games.  

# Network analysis

Network analysis is the key to creating private PlayStation servers. It allows us to see how the game protocol works. We can also get the order in which packets are sent and received, which is important for proper functionality.

## Tools for network analysis

## [Wireshark](https://www.wireshark.org/)

![Wireshark](https://upload.wikimedia.org/wikipedia/commons/c/cf/Wireshark_3.6_screenshot.png)

---

> Wireshark is a free and open-source packet analyzer. It is used for network troubleshooting, analysis, software and communications protocol development, and education.  
> [(from Wikipedia)](https://en.wikipedia.org/wiki/Wireshark)

Wireshark is a network traffic analysis tool. With this tool you can open packet captrues and view all ongoing communication. This tool comes in handy if you are working on creating private servers, as network communication is crucial for creating servers.  
games.  