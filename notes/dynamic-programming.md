---
tags: cs-374 algorithms
---

# Dynamic Programming

**Dynamic programming (DP)** is a technique for defining [[algorithm]]s that solve problems by breaking them down into simpler subproblems, which are computed and _stored_ for quicker lookup and better overall [[runtime]].

DP problems are usually derived from an initial recursive solution, which are modified to use DP to store computed subproblems.

## Solution Structure

The following questions outline a method of solving a [[backtracking]] problem using dynamic programming:

1. Can we do **recursion**? Where?
2. What is our **recursive subproblem**? (in English) i.e. what is the **recurrence**?
3. Let's do recursion!
   - What are the **base cases**?
   - What are the **recursive steps**?
4. How do we calculate our **final answer**?
5. For DP, what is the best **memoization** structure?
6. What are our **dependencies** at each step in the recurrence?
7. Using our memoization structure, where can we find our final answer?
8. What is the runtime of this solution?
