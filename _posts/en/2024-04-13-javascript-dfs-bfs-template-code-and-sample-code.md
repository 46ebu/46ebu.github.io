---
title: "[javascript] dfs bfs template code and sample code"
author: 46ebu
date: 2024-04-13 00:39:09 +0000
categories: [javascript]
tags: [javascript]
render_with_liquid: false
---

![Intro](/assets/img/post/javascript.png)
### Introduction
Depth-first search (DFS) and breadth-first search (BFS) are common algorithms used in graph traversal. In this blog post, we will explore template code for implementing DFS and BFS in JavaScript. We will also provide sample code examples to help you understand how these algorithms work.

### DFS Template Code
DFS is a recursive algorithm that explores as far as possible along each branch before backtracking. Here is a template code for DFS in JavaScript:

```javascript
function dfs(node, visited) {
    if (visited.has(node)) return;
    
    visited.add(node);
    
    // Perform actions on the current node
    
    for (let neighbor of node.neighbors) {
        dfs(neighbor, visited);
    }
}
```

### BFS Template Code
BFS explores nodes level by level, using a queue data structure. Here is a template code for BFS in JavaScript:

```javascript
function bfs(startNode) {
    let queue = [startNode];
    let visited = new Set();
    
    while (queue.length > 0) {
        let currentNode = queue.shift();
        
        // Perform actions on the current node
        
        visited.add(currentNode);
        
        for (let neighbor of currentNode.neighbors) {
            if (!visited.has(neighbor)) {
                queue.push(neighbor);   
            }
        }
    }
}
```

### Sample Code Examples
Let's consider a simple graph represented as an adjacency list to demonstrate DFS and BFS in action:

```javascript
const graph = {
    0: [1, 2],
    1: [0, 3, 4],
    2: [0],
    3: [1],
    4: [1],
};

const startNode = 0;
let visited = new Set();
dfs(startNode, visited);
```

The output of the DFS algorithm on this graph would be the nodes visited in the following order: 0, 1, 3, 4, 2.

```javascript
let visited = new Set();
bfs(0);
```

The output of the BFS algorithm on this graph would be the nodes visited in the following order: 0, 1, 2, 3, 4.

### Conclusion
In this blog post, we explored template code for DFS and BFS in JavaScript, along with sample code examples. These algorithms are fundamental in graph theory and can be used to solve a variety of problems related to graph traversal. By understanding how DFS and BFS work, you can implement them in your own projects to solve complex graph-related tasks efficiently.