---
title: "[go] dfs bfs template code and sample code"
author: 46ebu
date: 2024-04-13 00:39:36 +0000
categories: [go]
tags: [go]
render_with_liquid: false
---

![Intro](/assets/img/post/go.png)
### Introduction
Depth-First Search (DFS) and Breadth-First Search (BFS) are fundamental algorithms in graph theory. These algorithms are commonly used in various applications such as pathfinding, network analysis, and more. In this blog post, we will explore DFS BFS template code and provide sample implementations in Golang.

### DFS Template Code
DFS is a recursive algorithm that explores the graph as deeply as possible along each branch before backtracking. The template code for DFS in Golang typically involves a visited map to keep track of visited vertices and a recursive function to traverse the graph. Here is a basic template for DFS:

```go
func dfs(node int, visited map[int]bool, graph [][]int) {
	visited[node] = true
	// Process the current node
	for _, neighbour := range graph[node] {
		if !visited[neighbour] {
			dfs(neighbour, visited, graph)
		}
	}
}
```

### BFS Template Code
BFS is an algorithm that explores the graph level by level. It uses a queue data structure to keep track of vertices to visit next. The template code for BFS in Golang typically involves a queue to store vertices to visit and a loop to process the nodes. Here is a basic template for BFS:

```go
func bfs(start int, graph [][]int) {
	queue := []int{start}
	visited := make(map[int]bool)
	visited[start] = true

	for len(queue) > 0 {
		node := queue[0]
		queue = queue[1:]
		// Process the current node
		for _, neighbour := range graph[node] {
			if !visited[neighbour] {
				visited[neighbour] = true
				queue = append(queue, neighbour)
			}
		}
	}
}
```

### Sample Code and Output
Consider the following graph represented as an adjacency list:

```
graph := [][]int{
	{1, 2},
	{0, 3, 4},
	{0},
	{1},
	{1},
}
```

If we run the DFS and BFS functions on this graph, we can see the following outputs:

- DFS traversal: 0 -> 1 -> 3 -> 4 -> 2
- BFS traversal: 0 -> 1 -> 2 -> 3 -> 4

These traversals show how DFS explores the graph depth-first while BFS explores it level by level.

### Conclusion
In this blog post, we have covered the DFS BFS template code in Golang along with sample implementations and outputs. Understanding these algorithms and their implementations in Golang can be beneficial for solving graph-related problems efficiently. By utilizing these template codes and concepts, you can apply DFS and BFS in a wide range of scenarios.