---
layout: project
type: project
image: images/sudokuheadersmall.png
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

You can view the source code on [github](https://github.com/acjones8/Sudoku-Solver). A sample of the solver's output is below, but it may not display properly if your browser reformats te text width.

    solving example 1
    +---------+---------+---------+---------+
    | B 2 5   | 4   9   | 6 E   1 |   3     |
    | E   0 9 |     2 C | D   3   | F       |
    | 1       |     7   |   9   2 | B 5 E 0 |
    | D 8     | 5     0 |     F   |   9   2 |
    +---------+---------+---------+---------+
    | 0 7 E 2 |       9 |       5 |     3 F |
    | 3       | A       | 2 4 D F |     6 B |
    | C   A D |         | 8       | 7   5 9 |
    | 6 B     |   F     |   C 9 3 |     A   |
    +---------+---------+---------+---------+
    | 2       | 3 7 B 4 | 5       | 0 D   8 |
    | 7 6 C 8 |         | 0 D   B | 4       |
    | 4 9 3   |         | F   C 7 | 6   1   |
    | A   B   | F   C 1 | 3     E | 9 7     |
    +---------+---------+---------+---------+
    | 9   2   | 7 4 0   |     5   |   8 D   |
    | 8 3 7   |   9 6   | C       |       E |
    | F   4   | C   8 A |         | 1 6 9 7 |
    | 5 C   6 |   3 F   | 9 0     | 2       |
    +---------+---------+---------+---------+
    
    success!
    +---------+---------+---------+---------+
    | B 2 5 7 | 4 A 9 F | 6 E 0 1 | C 3 8 D |
    | E 4 0 9 | 8 B 2 C | D 5 3 A | F 1 7 6 |
    | 1 A F C | 6 D 7 3 | 4 9 8 2 | B 5 E 0 |
    | D 8 6 3 | 5 E 1 0 | B 7 F C | A 9 4 2 |
    +---------+---------+---------+---------+
    | 0 7 E 2 | B 8 4 9 | 1 6 A 5 | D C 3 F |
    | 3 5 9 1 | A C E 7 | 2 4 D F | 8 0 6 B |
    | C F A D | 2 1 3 6 | 8 B E 0 | 7 4 5 9 |
    | 6 B 8 4 | 0 F 5 D | 7 C 9 3 | E 2 A 1 |
    +---------+---------+---------+---------+
    | 2 E 1 F | 3 7 B 4 | 5 A 6 9 | 0 D C 8 |
    | 7 6 C 8 | 9 2 A 5 | 0 D 1 B | 4 E F 3 |
    | 4 9 3 5 | E 0 D 8 | F 2 C 7 | 6 B 1 A |
    | A D B 0 | F 6 C 1 | 3 8 4 E | 9 7 2 5 |
    +---------+---------+---------+---------+
    | 9 1 2 E | 7 4 0 B | A F 5 6 | 3 8 D C |
    | 8 3 7 A | D 9 6 2 | C 1 B 4 | 5 F 0 E |
    | F 0 4 B | C 5 8 A | E 3 2 D | 1 6 9 7 |
    | 5 C D 6 | 1 3 F E | 9 0 7 8 | 2 A B 4 |
    +---------+---------+---------+---------+
    
    given solution:
    +---------+---------+---------+---------+
    | B 2 5 7 | 4 A 9 F | 6 E 0 1 | C 3 8 D |
    | E 4 0 9 | B 8 2 C | D 5 3 A | F 1 7 6 |
    | 1 A F C | 6 D 7 3 | 4 9 8 2 | B 5 E 0 |
    | D 8 6 3 | 5 E 1 0 | B 7 F C | A 9 4 2 |
    +---------+---------+---------+---------+
    | 0 7 E 2 | 8 B 4 9 | 1 6 A 5 | D C 3 F |
    | 3 5 9 1 | A C E 7 | 2 4 D F | 8 0 6 B |
    | C F A D | 2 1 3 6 | 8 B E 0 | 7 4 5 9 |
    | 6 B 8 4 | 0 F 5 D | 7 C 9 3 | E 2 A 1 |
    +---------+---------+---------+---------+
    | 2 E 1 F | 3 7 B 4 | 5 A 6 9 | 0 D C 8 |
    | 7 6 C 8 | 9 2 A 5 | 0 D 1 B | 4 E F 3 |
    | 4 9 3 5 | E 0 D 8 | F 2 C 7 | 6 B 1 A |
    | A D B 0 | F 6 C 1 | 3 8 4 E | 9 7 2 5 |
    +---------+---------+---------+---------+
    | 9 1 2 E | 7 4 0 B | A F 5 6 | 3 8 D C |
    | 8 3 7 A | D 9 6 2 | C 1 B 4 | 5 F 0 E |
    | F 0 4 B | C 5 8 A | E 3 2 D | 1 6 9 7 |
    | 5 C D 6 | 1 3 F E | 9 0 7 8 | 2 A B 4 |
    +---------+---------+---------+---------+
    
    difference between solutions:
    +---------+---------+---------+---------+
    | B 2 5 7 | 4 A 9 F | 6 E 0 1 | C 3 8 D |
    | E 4 0 9 |     2 C | D 5 3 A | F 1 7 6 |
    | 1 A F C | 6 D 7 3 | 4 9 8 2 | B 5 E 0 |
    | D 8 6 3 | 5 E 1 0 | B 7 F C | A 9 4 2 |
    +---------+---------+---------+---------+
    | 0 7 E 2 |     4 9 | 1 6 A 5 | D C 3 F |
    | 3 5 9 1 | A C E 7 | 2 4 D F | 8 0 6 B |
    | C F A D | 2 1 3 6 | 8 B E 0 | 7 4 5 9 |
    | 6 B 8 4 | 0 F 5 D | 7 C 9 3 | E 2 A 1 |
    +---------+---------+---------+---------+
    | 2 E 1 F | 3 7 B 4 | 5 A 6 9 | 0 D C 8 |
    | 7 6 C 8 | 9 2 A 5 | 0 D 1 B | 4 E F 3 |
    | 4 9 3 5 | E 0 D 8 | F 2 C 7 | 6 B 1 A |
    | A D B 0 | F 6 C 1 | 3 8 4 E | 9 7 2 5 |
    +---------+---------+---------+---------+
    | 9 1 2 E | 7 4 0 B | A F 5 6 | 3 8 D C |
    | 8 3 7 A | D 9 6 2 | C 1 B 4 | 5 F 0 E |
    | F 0 4 B | C 5 8 A | E 3 2 D | 1 6 9 7 |
    | 5 C D 6 | 1 3 F E | 9 0 7 8 | 2 A B 4 |
    +---------+---------+---------+---------+
     
    solving example 2
    +---------+---------+---------+---------+
    | 4     9 |   E   0 |       6 |         |
    | 3     2 |         |   8 5 B | A 0   E |
    | D       | A 2 8   | 1 C     |     9   |
    | A 7     | 4   3 F |         |   8   C |
    +---------+---------+---------+---------+
    | 5   3   |   C 4   | D       |   B     |
    | E       |   0   D | F   9   | 6 3 8   |
    | 7 8   F |   3 1 A | E     4 |   5     |
    | B A 1   |     9   |         |     0 4 |
    +---------+---------+---------+---------+
    | 9 3 D   | 7 8 F   | 6     0 |   E     |
    | 8   F 1 |         | 5     E | 0 C A   |
    | 6     E | C A     | 3   F D | 8   1 7 |
    | 0     7 |     2 1 |       8 | F       |
    +---------+---------+---------+---------+
    | C 0 7   | 8   B   | A   1   | 5       |
    | 1 6     |     5 2 |       7 | B A F   |
    | 2   E 5 | D   A   |     4   | 9   7 8 |
    | F   9 A |   1     |   2     |   6 4   |
    +---------+---------+---------+---------+



