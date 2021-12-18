---
layout: essay
type: essay
title: Style with Substance
date: 2021-09-23
labels:
    - linters
    - coding standards
    - formatting
    - best practices
---
#The value of standards
This week in my Introduction to Software Engineering class, one of
the main focuses we covered was on coding standards and their
importance. Coding standards isn’t just limited to the level of
indentation or where to place braces; it also includes standards on
how to approach certain problems. In my case, this covered situations
such as when to approach a problem from a functional or object
oriented perspective, and the advantages and disadvantages of each.
One such example is, we recently needed to create a function that
merged two lists, either of identical or differing lengths. During it
manually in an iterative approach in plain Javascript, the solution
was rather ugly and looked something like this (in psuedocode):
```
shorter_length = min(list a, list b);
final_list = []
for (int i = 0; i < shorter; i++)
        final_list.append(list a[i]);
        final_list.append(list b[i]);
```
and then depending on the value of whether list a is shorter or not,
we needed a second for loop to iterate through the remaining list.
It’s pretty verbose and rather ugly. In contrast, with the help of
Underscore, it boiled down to a very simple:
```
return _.flatten(_.zip(list a, list b))
```
a one line piece of code that avoided having to worry about edge cases
like whether one list is shorter or longer.

#The value for collaboration
But coding standards are important not just for our own use in
approaching code, but it’s also critical in helping people with
greatly different coding styles work together. In my case for example,
I’m a big fan of the Allman style of formatting, by putting braces on
their own lines and using generous spacing, and in addition I tend to
approach problems in an imperative, object oriented manner, as my
first languages (Python, C, and Java) are all imperative object
oriented programming languages. Someone else who started with
functional languages however, such as Lisp, may prefer a far terser,
more functional programming style, even when both of us are using the
same language (in this case, Javascript). Having a shared set of
coding standards and an agreement about how we’re going to approach
problems makes for a much more cohesive program, and I can already see
this is going to be a critical skill when we get to our group project.

#Automated Enforcement
In our particular case, we’ve been working not just with a set of
style guides, but also with a linter, ESlint. ESlint’s job is to make
sure our code is structured in an appropriate manner, and it points
out mistakes or alternatives where we can approach things differently.
There are a few suggestions I’ve found to be rather useless – in
particular, needing to maintain one, and only one, empty line at the
end of the file. Given that a few newlines takes up a negligible
amount of space, I personally don’t think the distraction is worth
saving a few bytes. On the whole though, ESlint has been an enormously
helpful tool that enforces a level of consistency I know I would never
be able to maintain without its help, and it (or linters in general)
are going to be a core part of my toolkit for future programming.
Learning practices like this is exactly why I decided to pursue a
Computer Science degree, and it’s very satisfying to be learning these
techniques that will be directly applicable once we graduate.
