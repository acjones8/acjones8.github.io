<!---

---
layout: essay
type: essay
title: The difficult things will always be difficult
# All dates must be YYYY-MM-DD format!
date: 2016-02-06
labels:
  - Engineering
---

<img class="ui tiny right spaced image" src="../images/degree_difficulty.jpg">*Difficulty: a thing that is hard to accomplish, deal with, or understand.*

One of my friends asked the question earlier last week -- why is it so hard to be an officer for the student branch? Why is so hard compared to working at my on-campus job? This question came after he struggled a little with bookkeeping for the student organization.

Now I gave him the standard answer - being an officer of an organization requires that you manage your time between school and work. There isn't anyone telling you what to do. It's the answer any good mentor would give, and is mostly true.

But the more I though about it, the more I wondered to myself...damn that's a really great question; it's one that deserves some more thought. Most people I think stop at the answer I gave previously - he obviously isn't managing his time properly.

Here's what I think: the difficult things will always be difficult.

## In the context of programming

In the context of programming, this has always been true. The difficult problems have always been different, although changes in technology can change the landscape quite a bit. "Business" type applications are the things that come to mind for me. Those types of applications are usually coupled in some way with people ... and people are awfully hard to deal with!

Consider that one of the most popular content management systems is also considered the most horrible - Wordpress. But really, is there anything that fills that need? If it was so easy in the first place, where is the solution? Where's the magic CMS that is designed well enough that everyone hops on the boat to use it?

Some things are just difficult - building applications that humans use is hard, and will probably be hard for at least the near future.

## In the context of engineering

Ever hear people ragging on engineering companies for delivering late and way over budget? Well, some engineering jobs are really difficult, especially if the requirements and funding are undulating underneath you. Because of the nature of the problem, sometimes engineering firms require large amounts of engineers and workers, inviting further problems and delays.

The Honolulu Rail project at home has become this sort of poster child of failure, budget overrun and overall incompetence in Hawaii. Well, working though regulatory boards and fiscal procedures in Hawaii seems like it's a mind bogglingly difficult job to do. Granted, there might be some fishy stuff going on, but I refuse to believe that everyone is involved for nefarious reasons.

The problem of creating an unprecedented public transportation backbone on an island is difficult! I'm not sure we would have done it right, even if the best people were involved.

## In the context of relationships

So in the end, we realize that all engineering and programming is there for a reason - to serve human needs. Maybe that's why those things are difficult, because they both involve humans and are for humans.

Relationships, regardless if they're romantic or not take work. Humans are fickle creatures and relationships can come and go with the wind. To properly maintain something over time requires work. Family takes work. Marriage takes work. We live to figure out what works and what doesn't and hope that as we move forward we're improving.

Relationships have always been difficult, and by nature will continue to be so.

## Okay!

So back to the original premise; why is being one of the club officers so difficult?

And the final answer - it's supposed to be difficult, and it's supposed to challenge you, just like everything else that humans do that is difficult: programming, engineering, engaging in relationships, pondering the universe, etc.

Ultimately the question you should really ask yourself if something if particularly difficult is then "is it worth it"? That is something that is context specific and only you can answer yourself.


--->

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
