# Number of Islands - W13D4

## Problem

Given a 2D grid of binary numbers that represent a map of `1`s (land) and `0`s (water), return number of islands. Islands are surrounded by water and are connected `1`'s horizontally or vertically.

## Approach

Depth-First Search (DFS) checks each island. When `1` found, DFS marks all connecting `1`'s as checked. This way, number of islands can be counted.

1. Check if empty grid - return `0`.
2. Initialize the `num_islands` to `0`.
3. Helper function marks connected land as checked using DFS to mark connected land.
4. Iterate through each cell in grid
    - If land, increment number of islands and use helper function to mark connected land as checked.
5. Return the number of islands.

## Optimization

- Time complexity O(m*n), where m is number of rows and n is number of columns, because each cell is checked once.
- Space complexity also O(m*n) because of recursion stack used for DFS.
