# Advent Of Code 2024

Update private input module with: `git submodule update --init --remote --recursive`

* [Day 1](Day01.ipynb). Easy list manipulation, solution is trivial with `sort` and `numpy` vector algebra.

* [Day 2](Day02.ipynb). Array manipulation, `numpy` FTW.

* [Day 3](Day03.ipynb). String manipilation with regular expressions (I tried to use regexp to a maximum to avoid explicit searching).

* [Day 4](Day04.ipynb). First 2D map of the year! Using a `defaultdict` to store map information to void having to check boundaries, with complex number to represent coordinate to simplify movements as operations on complex values.

* [Day 5](Day05.ipynb). Custom `compare` function following the ordering rules, to be passed to sorting algorithm via `functools.cmp_to_key()`

* [Day 6](Day06.ipynb). 2D map exploration with rotation at obstacles. Using complex number to describe positions and (change of) directions, map represented as dictionary to simplyfy boundary checks. Part 2 requires identification of loop, tracked with recurring positions and direction. Initially tested all position on map to place obstacles (~42s execution on my laptop), then realised I only need to place them on the initial path of the guard (this reduces the execution time to ~7s).

* [Day 7](Day07.ipynb). Mathematical operations to be evaluated in sequential order to find permutation giving right result. There might be some mathematical shortcut, but I went for the brute force solution. I was initially using `eval` to make calculation to save a `if` structure, but `eval` is very slow and makes part 2 solution very long. Swithcing to pure mathematical functions speeds things up considerably.

* [Day 8](Day08.ipynb). Line tracing on a 2D grid.

* [Day 9](Day09.ipynb). Long list with elements to be updated. Used a `dictionary` for faster lookup, considered for a moment to write a custom linked-list class fearing what could come up in part 2, but ended up bruteforcing part 2 in ~1 minute with some basic optimizations.

* [Day 10](Day10.ipynb). Path finding with BFS.

* [Day 11](Day11.ipynb). Stone ordering is irrelevant (new stones only depend on current stone value), so the operation on stones with same value can be factorised (not sotring all stones, but only their relelative occurrencies), and this allows to solve Part 2.

* [Day 12](Day12.ipynb). Recursive flood fill for Part 1. Part 2 was tricky: I got the idea of finding vertices by projecting the square centers pretty quickly, but to find the correction needed to account for concave patches I had to make drawings, see the missing vertices, and then count by hand to understand how to properly account sides associated by vertices sharing diagonal squares.

* [Day 13](Day13.ipynb). Solved Part 1 with brute force, expecting Part 2 to make it impossible. After some pondering (and even thinking about diophantine equations) I realised the problem can be reduced as a system of two linear equations with two unknowns, relatively simple to solve!

* [Day 14](Day14.ipynb). Part 1 was a simple evolution of points on a grid. Part 2 was... unexpected! Initially solved by scanning many frame rendering by eye, later tried a couple of different approaches, including image entropy.

* [Day 15](Day15.ipynb). Grid navigation and collision detection. BFS for vertical movements of Part 2 to build list of box coordinated to be moved.

* [Day 16](Day16.ipynb). Path finding with movement weight: using Dijkstra's algorithm with a `PriorityQueue` indexed on path score. For Part 2 saving full path and accumulating all positions for paths with best scores, returning the total set when best score is exceeded (i.e. all best score paths are found).

* [Day 17](Day17.ipynb). Simple opcode for Part 1. To solve Part 2 I reverse-engineered the program to understand the lnk between input register and output, then implemented a recursive search for the input value components (in base 8) that resulted in an output mimicking the program itself.

* [Day 18](Day18.ipynb). BFS for Part 1, brute force scanning for Part 2.

* [Day 19](Day19.ipynb). Recursion and backtracking to find the sequences of strings composing input strings. Memoization already needed to converge on Part 1. I initially was finding the actual sequences (works fine for Part 1 with memoization), but this explodes for part 2, where simply counting all possible sequence is instead feasible.

* [Day 20](Day20.ipynb). Path navigation with a spin. One might be tempted to use a path finding algorithm on this, but since the initial path is unique one can cache all distances to the end, and "recompose" the path distance after the cheat by summing the partial distances and the cheat lenght.

* [Day 21](Day21.ipynb). I had the good idea to use `networkx` to simplfy the search for the shortest paths, but building the full sequence string only worked for Part 1. For Part 2 I cached all shortest paths between any key on both keypads, then recursively counted the shortest sequence lenght by reaching the bottom of the robot chain, where the sequence themselves can be converted into their lenght and propagated up through the recursion chain. Today was as difficult as Day 19, and in some sense similar in what the solution for part 2 needed.

* [Day 22](Day22.ipynb). Linear Congruential Generator, list and dictionary manipulation.

* [Day 23](Day23.ipynb). Graph manipulation: using a dictionary for Part 1, `networkx` FTW for Part 2!