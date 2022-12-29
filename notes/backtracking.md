---
tags: cs-374 algorithms
---

# Backtracking

**Backtracking** is a recursive strategy for implementing [[algorithm]]s that try to construct a solution to a computational problem incrementally, recursively evaluating _every_ possible next component and choosing the best one to solve the problem.

Examples:

- N Queens
- Game Trees (abstract structure for any game)
- Subset Sum
- Text Segmentation
- Longest Increasing Subsequence
- Optimal Binary Search Trees

## Solution Structure

The following questions outline a method of solving a backtracking problem:

1. Can we do recursion? Where?
2. What is our recursive subproblem? (in English)
3. Let's do recursion!
   - What are the base cases?
   - What are the recursive steps?
4. How do we calculate our final answer?

## Analysis

Backtracking algorithms have exponential worst-case [[runtime]]s.
