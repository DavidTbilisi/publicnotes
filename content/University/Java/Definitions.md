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
**String literal** - zero or more characters enclosed in double quotes <br/>
**Statement** - complete instruction that tells a program to do something <br/>
**Expression** - coding construct that produces a single value when evaluated <br/>



**JDK** - Java Development Kit <br/>
**JRE** - Java Runtime Environment <br/>
**JVM** - Java Virtual Machine <br/>


![](https://media.geeksforgeeks.org/wp-content/uploads/20251003165228816476/jvm.webp)


| Aspect              | JDK                                             | JRE                                    | JVM                                                        |
| ------------------- | ----------------------------------------------- | -------------------------------------- | ---------------------------------------------------------- |
| Purpose             | ==develop== Java applications                   | ==Run== Java applications              | ==Executes== Java bytecode                                 |
| Platform Dependency | OS specific                                     | OS specific                            | JVM is OS-specific, bytecode is platform-independent       |
| Includes            | JRE + Development tools (javac, debugger, etc.) | JVM + Libraries (e.g., rt.jar)         | ClassLoader, JIT(Just In Time) Compiler, Garbage Collector |
| Use Case            | Writing and compiling Java code                 | Running a Java application on a system | Convert bytecode into native machine code                  |
