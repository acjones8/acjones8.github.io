---
layout: essay
type: essay
title: No Bad Questions? StackOverflow Disagrees
# All dates must be YYYY-MM-DD format!
date: 2021-09-09
labels:
  - Questions
  - StackOverflow
---

No Bad Questions? Stack Overflow Disagrees


This week in my software engineering class, one of the topics we
covered was the importance of asking questions in a helpful and
precise manner that makes it easy for others to assist in finding a
solution, instead of questions that are vague or lack helpful
information. Programming (and working with IT in general) is a job
that’s extremely knowledge dependent, and no one is every going to
know everything about their environments; so being able to quickly
seek and receive help is critical to being successful.

An example of a question that’s asked in a smart manner, is ["RAII vs
Garbage Collection"](
https://stackoverflow.com/questions/44325085/raii-vs-garbage-collector)
(in C++ vs Java). RAII (Resource Acquisition Is Initialization) and
Garbage Collection are two different memory management paradigms; in
the former, the program allocates and deallocates memory for variables
and objects as soon as they come into scope, and deallocates them the
instant they go out of scope. In the latter, a sub-program called a
garbage collector monitors the memory space, and every so often
(depending on memory usage, time passed since the last round of
garbage collection, CPU usage, etc.) the garbage collector will
inspect all objects and variables in memory, and deallocate them in
bulk depending on if they have any valid references that indicate
they’re in use.

In this question, the person asking is seeking to understand the
difference between these two schemes and the advantages and
disadvantages of each. The asker mentions where they found out about
these terms (in a tech talk), allowing anyone answering to know the
context for themselves, and explains exactly what confuses them – why
there would be an advantage to having resources be allocated and
deallocated on demand, instead of in bulk.

In response, the question received numerous high-quality responses
that indicate some of the specific advantages to using RAII, as well
as some of the reasons to use a garbage collector – in particular, the
former is advantageous if the programmer wants to tightly control
exactly when memory is freed, which can be very important for timing
sensitive code. Examples of this would be in a video game, where every
frame must always be completed in less than 16.67ms to maintain smooth
performance, or in a real time setting such as a car’s ABS module,
which needs to be able to react with absolute certainty under a
certain amount of time. In these environments, the random delay of a
garbage collector is not acceptable. However, garbage collection can
have better performance in certain types of algorithms, and it can
handle certain situations such as circular references much better than
RAII can. This question provides a lot of useful answers to anyone
seeking to look into it, and if the original poster had simply asked a
single question in the title, it’s less likely that they would have
received so many good responses.

An example of a bad question is ["compile the R failed with Flang in
freeBSD"](https://stackoverflow.com/questions/67563059/compile-the-r-failed-with-flang-in-freebsd).
This is already off to a bad start; the question itself is vague and
doesn’t provide much detail, and it has grammatical and capitalization
errors in it. What the asker is asking here is for information about
why the program (the R programming environment) isn’t compiling; but
in the body, all they give is their configure command and a few lines
of the compilation from the body. Useful information that someone else
trying to help would want to know would be the version of R, what
they’ve tried to fix it so far and how that’s affected the error, and
in particular, why they’re not using FreeBSD’s built in math/R port
and instead trying to build it manually. FreeBSD’s port is a Makefile
that already specifies all the dependencies and can build the program
without any user input, so it’s very strange to see someone attempting
to do it manually.

As a result of not asking their question in a helpful manner, the
question has not received a singe response from the community; and
even if it did, the most likely question would be asking them why they
aren’t building from math/R. This is an answer that would just be
requesting the asker to put in information they should have done from
the beginning, which is slow and reduces people’s willingness to help,
if they have to ferret out a lot of details rather than having them
already provided.

Although it’s natural to ask poor questions with little experience – I
did so quite often when I was starting out with learning how to
program and administrate a Linux/Unix environment -, it greatly
increases the likelihood of getting useful responses if the question
provides helpful, detailed information up front. And so from my own
past mistakes, and from reading other people’s questions like this,
I’ve strived to try not to commit the same mistakes and ask
informative questions where possible.
