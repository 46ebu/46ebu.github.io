---
title: "[python] dfs bfs template code and sample code"
author: 46ebu
date: 2024-04-13 00:34:05 +0000
categories: [python]
tags: [python]
render_with_liquid: false
---

![Intro](/assets/img/post/python.png)
## Introduction
When it comes to solving graph-related problems, Depth-First Search (DFS) and Breadth-First Search (BFS) are two fundamental algorithms that are commonly used. In this blog post, we will delve into exploring template code for implementing DFS and BFS algorithms in Python.

### Depth-First Search (DFS)
DFS is a traversal algorithm used to visit all the nodes in a graph by exploring as far as possible along each branch before backtracking. It is implemented using a stack data structure. Here is a simple DFS template code in Python:

```python
def dfs(graph, start):
    stack = [start]
    visited = set()
    
    while stack:
        node = stack.pop()
        if node not in visited:
            visited.add(node)
            for neighbor in graph[node]:
                stack.append(neighbor)
    
    return visited
```

Let's consider a sample graph represented as an adjacency list:
```python
graph = {
    'A': ['B', 'C'],
    'B': ['D'],
    'C': ['E'],
    'D': [],
    'E': []
}
```

When we call `dfs(graph, 'A')`, it will output `{'A', 'B', 'D', 'C', 'E'}` as it visits all the nodes reachable from 'A' in depth-first order.

### Breadth-First Search (BFS)
BFS is another traversal algorithm that visits all the nodes in a graph level by level. It is implemented using a queue data structure. Below is a BFS template code in Python:

```python
from collections import deque

def bfs(graph, start):
    queue = deque([start])
    visited = set()
    
    while queue:
        node = queue.popleft()
        if node not in visited:
            visited.add(node)
            for neighbor in graph[node]:
                queue.append(neighbor)
    
    return visited
```

Let's use the same graph and call `bfs(graph, 'A')`. The output will be the same as DFS but in breadth-first order: `{'A', 'B', 'C', 'D', 'E'}`.

### Comparing DFS and BFS
Both DFS and BFS have their own advantages and use cases. DFS is more memory-efficient as it uses a stack and can be implemented using recursion. On the other hand, BFS guarantees the shortest path in an unweighted graph and is better suited for finding the shortest path.

### Conclusion
In this blog post, we have explored template code for implementing DFS and BFS algorithms in Python. These algorithms play a crucial role in graph traversal and have various applications in problem-solving. By understanding the template code provided, you can apply these algorithms to solve a wide range of graph-related problems.