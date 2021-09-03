---
layout: project
type: project
image: images/exapunks.png
title: Exapunks
permalink: projects/exapunks
# All dates must be YYYY-MM-DD format!
date: 2021-08-20
labels:
  - Assembly
  - Zachtronics
  - Game
summary: Exapunks is a game centered around programming, and this project follows my process in attempting to beat the game.
---

Zachtronics' EXAPUNKS is a programming game centered around the manipulation of small robotic agents called Exapunks. Zachtronics has made several other games in this genre, most notably TIS-100 and Shenzhen I/O, but my favorite of the bunch is Exapunks. Over summer 2021, I attempted a playthrough of the game, and although I haven't managed to fully complete it yet, I'm gotten fairly close.

One of the most interesting aspects of the game, is that it requires programming in a sort of psuedo-assembly unique to it, along with features such as parallel processing and communication between the different agents, which leads to needing to solve real world problems such as lock conention, optimizing for either speed or size, and implementing complex algorithems into assembly, a language which doesn't provide very much assistance to the programmer. The game comes with a manual that introduces many computing concepts in a very simplified way - for example, on one mission, you need to reprrogram the data broadcast for a satellite, and one of the satellite's protection mechanisms is an encryption key. Although the encryption implemented in the game is incredibly simplistic, the challenge of processing data while also encrypting it in transit is very much a real world problem. 

During the course of completing the game, I learned many valiable things - in particular, it was a great introduction to what programming in Assembly is like, and how far more complex programs from a higher level language such as C might be implemented. It also taught me how much room there is for optimization, as many of my solutions are not of maximal efficiency, and how poweful parellel computing can be - many of the missions can be completed in a small fraction of the time with clever use of multiple agents rather than a single agent that does everything. This is an increasingly relevant topic today in computer science, as even game consoles and low end laptops are starting to come standard with processors that feature 6 or more cores. In order to take full advantage of processors in the future, programmers will need to become increasingly comfortable with multithreading.

The solutions are uploaded as a series of text files [on GitHub](https://github.com/acjones8/Exapunks-Solutions).
