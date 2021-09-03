---
layout: project
type: project
image: images/sudoku.jpg
title: Recursive Sudoku Solver
permalink: projects/sudoku
# All dates must be YYYY-MM-DD format!
date: 2019-04-23
labels:
  - Recursion
  - Sudoku
  - Java
summary: For ICS 211, I completed a recursive sudoku solver that can solve any valid sudoku.
---

<!--
<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>
-->

For this assignment, the task was to implement the core logic in a sudoku solver - to recursively fill in the values of a sudoku puzzle, with or without any prexisting input, and then check the validity until either a solution was found or the puzzle was proven to be unsolvable. And for a fun twist, this sudoku solver is designed to work with hexadecimal, rather than the standard 0-9 decimal scale.

This was one of my first assignments that really required an understanding of how recusion worked, and it was quite challenging. I initially struggled to get it working correctly - it would constantly go out of bounds, or it wouldn't put in the right values into the puzzle. Eventually, I figured out the edge cases, and I thought I had a working program; however, when I actually ran the test cases, it provided subtly incorrect answers, or it wouldn't find a valid solution in puzzles that were known to have one. The culprit for this issue was eventually narrowed down to an off by 1 bug in the logic that called the next interation of the function, so that it would always skip over the 16th value, F. 

Once I finally got it working, all that was left to do was to make sure it could pass all of the test cases. We had 5 or 6 pre-provided sudoku puzzles, and while the first two completed nearly instantly, the 3rd and 4th ones took a few minutes. For the final hardest ones, it took my computer over half an hour to find a single valid solution, which also introduced me to the importance of algorithmic complexity and multithreading (as this sudoku solver is single thread only, it's unable to take advantage of most of the processor's computing power).

You can view the source code on [github](https://github.com/acjones8/Sudoku-Solver).



