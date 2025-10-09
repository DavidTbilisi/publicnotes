---
aliases:
title: Java vocabulary
draft: false
tags:
  - programming-languages
  - java
description:
permalink: https://www.geeksforgeeks.org/java/differences-jdk-jre-jvm/
date: 2025-10-09
---
**String literal** - zero or more characters enclosed in double quotes 

**Statement** - complete instruction that tells a program to do something

**Expression** - coding construct that produces a single value when evaluated



**JDK** - Java Development Kit

**JRE** - Java Runtime Environment

**JVM** - Java Virtual Machine


![](https://media.geeksforgeeks.org/wp-content/uploads/20251003165228816476/jvm.webp)


| Aspect              | JDK                                             | JRE                                    | JVM                                                        |
| ------------------- | ----------------------------------------------- | -------------------------------------- | ---------------------------------------------------------- |
| Purpose             | ==develop== Java applications                   | ==Run== Java applications              | ==Executes== Java bytecode                                 |
| Platform Dependency | OS specific                                     | OS specific                            | JVM is OS-specific, bytecode is platform-independent       |
| Includes            | JRE + Development tools (javac, debugger, etc.) | JVM + Libraries (e.g., rt.jar)         | ClassLoader, JIT(Just In Time) Compiler, Garbage Collector |
| Use Case            | Writing and compiling Java code                 | Running a Java application on a system | Convert bytecode into native machine code                  |
