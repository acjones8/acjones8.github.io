---
layout: project
type: project
# image: images/exapunksheadersquare.png
title: Multithreaded Java Image Editor
permalink: projects/java_parallel_img
# All dates must be YYYY-MM-DD format!
date: 2022-12-08
labels:
  - Java
  - Multithreading
  - Image Processing
summary: Modified a pre-written single threaded image processing program in Java, learning about concurrency and gaining substantial performance improvements over the initial template.
# published: false
---

For this project, the professor placed us in rotating groups, where we started with an initial program (either a template provided to us at the beginning of the seemster, or the results from another group's work the previous week), and we modified the program in order to implement new filters, add concurrency, and add features to the GUI. The program can apply several different image filters, such as a black and white conversion or an oil painting effect, to image files, and it can do so in parallel if the user wishes. It collects statistics in real time, such as the number of images processed, the average time taken to process an image, etc. and presents them to the user.

This was probably my favorite project that I did while at UH Manoa, for a number of reasons. Concurrency, at its core, is a really neat concept - you go from thinking about how a program steps through, and instead, now you have to think about how different copies of this same program interact with each other, and how it can be in different states simultaneously. There are many new bugs that can be introduced when adding concurrency, such as deadlocks (different threads get stuck waiting on each other to free or acquire a resource), starvation (a thread doesn't get an adequate amount of scheduled time, so its work isn't completed at an acceptable rate), and non-deterministic behavior (a program may not always react the same even when placed in exactly the same conditions, if threads can modify eac others' behavior). However, at the same time, concurrency is one of the few ways developers can still witness tremendous performance improvements, if the problem lends itself well to it. In this project for instance, I witnessed a 150% to nearly 400% performance improvement over the single threaded version, depending on the exact parameters specified (such as the number of threads, the filter, and whether the program was working on multiple different images or slicing the same image into smaller pieces).

Some significant challenges I encountered working on it were the classical concurrency problems mentioned above (in particular, I remember a particularly nasty deadlock that occured between the processing and writing threads only very ocassionally, due to accidentally freeing a lock slightly too early). In addition, we maintained the documentation within the code itself, and because our projects were passed around between different teams (each implementing only a single new set of features or capabilities), it mimicked a real world codebase were we had to work with code from people we didn't know.

Overal, I really enjoyed not only the project itself, but ICS 432 (Concurrency) as a class - I would say it was probably my favorite class I ever took at UH Manoa, and my understanding of concurrency and parallelism is something I've frequently applied since.
