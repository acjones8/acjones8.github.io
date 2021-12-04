---
layout: essay
type: essay
title: Doors over Docs
# All dates must be YYYY-MM-DD format!
date: 2021-12-03
labels:
  - Software Engineering
  - Design Patterns
---

There's a tool that virtually every programmer, around the world, uses every single day. This tool allows programmers to manage access to remote spaces, provides protection from prying eyes, and allows for the transfer of pretty much anything. The natural guess from most software engineers would be SSH, or perhaps a VPN, but I would suggest... the humble door. That's right, a piece of wood (or sometimes metal) suspended on a set of hinges from a frame.

#### How to use a door?

The first question you're probably asking yourself is "what does a door have to do with software development?" And indeed, there isn't much of a link at first glance. But both a door and a program have one thing in common; they need to be used by their end users, despite working in a variety of different ways. For example, there's your typical North American house door, which is just a hollow wooden plank with a standard twist handle. But there's also doors with a handle, push or pull doors with a metal bar, sliding doors, and even some really exotic kinds such as the ones on ships with a wheel that are designed to seal out water, or the revolving doors sometimes found at the entrances to large stores. And yet, despite the wide variety of shapes and sizes that doors come in, not a single one of them requires the end user to ever read an instruction manual or consult documentation on how it works.

#### A more detailed example

![A picture of a door with metallic push plates](https://www.barbourproductsearch.info/1.%20Mid%20Plates%20-%20Push%20and%20Kick%20Plates%20by%20Hafele1%20copy-file096608.jpg)

Perhaps my favorite example is the push door with a simple metal plate attached. This metal plate does precisely nothing functional at all; it doesn't provide structural rigidity, it doesn't give the user a better grip on the door, it doesn't provide any protection against unauthorized access. One could remove this metal plate, and the door would function exactly as it always has, with absolutely no compromises or changes in how it works. And yet, even though it serves absolutely no purpose for the door itself, it signals to people on what kind of door they're facing (a push door) and how to use it (merely push on the plate) - and remarkably, does this with absolutely zero symbols, writing, or any form of explicit communication at all. The mere presence of this plate *is* the communication. This plate is an example of a design pattern; designing things in a consistent way so that people know what it does and how it functions, without needing to study or consult documentation on how it works.

#### How this relates to software engineering

Much like door designers, software engineers use design patterns all the time, both for our own benefit and that of our end users. One such example is getters and setters in Java. In Java, there's a concept of privilege levels, and objects can be designed such that their data can only be accessed directly by themselves or their children. However, even if an object doesn't have direct access to anothers' instance variables, sometimes it's useful to still expose these through a standard interface. From this, arises `get` and `set`, which are standardized methods that allow programmers to retrieve a value without needing direct access to its private data. 

Another example of this is the navbar, a common feature on many websites. Many users are familiar with the concept of a bar at the top of the screen containing links to different pages on the website, and by using this pattern, the website's end users can quickly and efficiently see all of the main sections on the website, and quickly find the page they need, without having to ever look up any specific documentation for this site. 

In my time learning how to program, I've found that learning good design patterns is immensely beneficial - they provide an easy to understand and consistent solution to problems, and they make life significantly easier for both myself and the end user. And when design patterns are applied poorly, well, you get doors with signs that say "push" when the bar suggests "pull".

