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