# Advent Of Code 2024

Update private input module with: `git submodule update --init --remote --recursive`

* [Day 1](Day01.ipynb). Easy list manipulation, solution is trivial with `sort` and `numpy` vector algebra.

* [Day 2](Day02.ipynb). Array manipulation, `numpy` FTW.

* [Day 3](Day03.ipynb). String manipilation with regular expressions (I tried to use regexp to a maximum to avoid explicit searching).

* [Day 4](Day04.ipynb). First 2D map of the year! Using a `defaultdict` to store map information to void having to check boundaries, with complex number to represent coordinate to simplify movements as operations on complex values.

* [Day 5](Day05.ipynb). Custom `compare` function following the ordering rules, to be passed to sorting algorithm via `functools.cmp_to_key()`
