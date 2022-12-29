---
tags: algorithms computer-science graphs cs-374
---

# Depth first search

**Depth first search (DFS)** is an [[algorithm]] for traversing or searching graph-like data structures that starts at a root node and explores as far as possible along each branch before backtracking.

- good for exploring graph like structures

It can be implemented iteratively with a stack or more simply recursively.

## Recursive pseudocode

```text
DFS(v):
  if v is unmarked
    mark v
    for each edge v -> w
      DFS(w)
```

## Sources

- <https://en.wikipedia.org/wiki/Depth-first_search>
- <https://jeffe.cs.illinois.edu/teaching/algorithms/book/06-dfs.pdf>
- <https://courses.engr.illinois.edu/cs473/sp2011/lectures/03_class.pdf>
