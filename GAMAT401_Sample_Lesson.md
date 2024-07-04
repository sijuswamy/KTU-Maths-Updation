# Graph Definition and Terminologies

## Lesson Objective
Upon successful completion of the session, the student will be able to:
- Understand the fundamental definitions and terminologies in graph theory.
- Differentiate between simple graphs, finite and infinite graphs, and null graphs.
- Represent and visualize these graphs using Python.

## Introduction
Graph theory is a branch of mathematics that studies the relationships between objects. A graph is a collection of points, called vertices, connected by lines called edges. Graphs are used to model pairwise relations between objects, making them a powerful tool for solving problems in computer science, such as network analysis, scheduling, and optimization.

## Presentation of the Idea and Concept

### Formal Definitions
1. **Vertex (Node)**: A vertex is a fundamental unit of a graph, representing an object. Formally, a vertex is an element of the set $\mathbf{V}$ of vertices.
2. **Edge (Link)**: An edge is a connection between two vertices in a graph. Formally, an edge is an element of the set $\mathbf{E}$ of edges, where each edge $e \in \mathbf{E}$ is an unordered pair of vertices $(u, v)$ for an undirected graph, or an ordered pair $(u, v)$ for a directed graph.
3. **Graph**: A graph $\mathbf{G}$ is defined as an ordered pair $\mathbf{G} = (\mathbf{V}, \mathbf{E})$, where $\mathbf{V}$ is a set of vertices and $\mathbf{E}$ is a set of edges connecting pairs of vertices.

### Simple Graph
A simple graph is an unweighted, undirected graph containing no loops (edges connected at both ends to the same vertex) or multiple edges (more than one edge between any two vertices). Each edge connects two different vertices.

**Example:**
Consider a social network where people are vertices, and friendships are edges. A simple graph can represent this network, where each person is connected to their friends by edges.
<>

```python
import networkx as nx
import matplotlib.pyplot as plt

# Create a simple graph
G = nx.Graph()
G.add_edges_from([(1, 2), (1, 3), (2, 3), (3, 4)])

# Draw the graph
nx.draw(G, with_labels=True, node_color='lightblue', edge_color='gray')
plt.title("Simple Graph")
plt.savefig("simple_graph.png")
plt.show()
```
