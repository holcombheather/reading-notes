# Graphs Cheat Sheet

**1. Terminology:**
- **Vertex (Node)**: A data object in the graph.
- **Edge (Arc)**: A connection between two vertices.
- **Weight**: A value (cost, distance, etc.) assigned to an edge.
- **Path**: A sequence of edges connecting two vertices.
- **Cycle**: A path that starts and ends at the same vertex.
- **Directed Graph (Digraph)**: A graph in which edges have a direction.
- **Undirected Graph**: A graph in which edges do not have a direction.

**2. Representing Graphs:**
- **Adjacency Matrix**: A 2D array where the cell M[i][j] represents the edge between vertices i and j.
- **Adjacency List**: An array of lists. The index represents the vertex and each entry in its list represents the vertices it's connected to.

**3. Creating a Graph:**

In JavaScript, we can represent a graph using an Object for the Adjacency List:

```javascript
class Graph {
  constructor() {
    this.nodes = {};
  }

  addVertex(vertex) {
    if (!this.nodes[vertex]) this.nodes[vertex] = [];
  }

  addEdge(v1, v2) {
    this.nodes[v1].push(v2);
    this.nodes[v2].push(v1);
  }
}
```

**4. Traversing Graphs:**
- **Breadth-First Search (BFS)**: It starts at the tree root and explores the neighbor nodes at the present depth prior to moving on to nodes at the next depth level.
- **Depth-First Search (DFS)**: It starts at the root (selecting some arbitrary node as the root in the case of a graph) and explores as far as possible along each branch before backtracking.

```javascript
// BFS
bfs(start) {
  const queue = [start];
  const visited = new Set(queue);

  while (queue.length) {
    const vertex = queue.shift();
    console.log(vertex);

    this.nodes[vertex].forEach(node => {
      if (!visited.has(node)) {
        queue.push(node);
        visited.add(node);
      }
    });
  }
}

// DFS
dfs(start, visited = new Set()) {
  console.log(start);
  visited.add(start);

  this.nodes[start].forEach(node => {
    if (!visited.has(node)) {
      this.dfs(node, visited);
    }
  });
}
```

**5. Graph Algorithms:**
- **Dijkstra's Algorithm**: Finds the shortest path between two vertices.
- **A* Search Algorithm**: Finds the shortest path between vertices, using a heuristic to guide the process.
- **Floyd-Warshall Algorithm**: Finds shortest paths between all pairs of vertices.
- **Kruskal's Algorithm**: Finds a minimum spanning tree for a connected weighted graph.
- **Prim's Algorithm**: Also finds a minimum spanning tree for a connected weighted graph.