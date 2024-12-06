# Advent Of Code 2024

Update private input module with: `git submodule update --init --remote --recursive`

* [Day 1](Day01.ipynb). Easy list manipulation, solution is trivial with `sort` and `numpy` vector algebra.

* [Day 2](Day02.ipynb). Array manipulation, `numpy` FTW.

* [Day 3](Day03.ipynb). String manipilation with regular expressions (I tried to use regexp to a maximum to avoid explicit searching).

* [Day 4](Day04.ipynb). First 2D map of the year! Using a `defaultdict` to store map information to void having to check boundaries, with complex number to represent coordinate to simplify movements as operations on complex values.

* [Day 5](Day05.ipynb). Custom `compare` function following the ordering rules, to be passed to sorting algorithm via `functools.cmp_to_key()`

* [Day 6](Day06.ipynb). 2D map exploration with rotation at obstacles. Using complex number to describe positions and (change of) directions, map represented as dictionary to simplyfy boundary checks. Part 2 requires identification of loop, tracked with recurring positions and direction. Initially tested all position on map to place obstacles (~42s execution on my laptop), then realised I only need to place them on the initial path of the guard (this reduces the execution time to ~7s).
