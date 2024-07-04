# DIY: Analyzing a Social Network of University Students Using Graph Theory

## Problem Statement
A university's computer science department wants to analyze the friendships among its students to better understand the social dynamics and identify students who might need additional social support. You are provided with a list of friendships, where each friendship is represented as a pair of student IDs as -(1, 2), (1, 3), (2, 4), (2, 5), (3, 6), (4, 7), (5, 8), (6, 9), (7, 10), (8, 11), (9, 12), (10, 13), (11, 14), (12, 15), (13, 16), (14, 17), (15, 18),(16, 19), (17, 20), (18, 21), (19, 22), (20, 23), (21, 24), (22, 25), (23, 26), (24, 27), (25, 28), (26, 29), (27, 30), (28, 31), (29, 32), (30, 33), (31, 34), (32, 35), (33, 1). Your tasks are to represent this social network as a graph, identify key properties of the graph (such as vertex degrees, isolated vertices, and pendant vertices), visualize the graph, and interpret the results to provide insights into the social network.

## Variables
- **Students (Vertices)**: Represented by unique IDs.
- **Friendships (Edges)**: Each friendship is an undirected edge between two students.

## Sub Tasks
1. **Graph Representation**:
   - Create a graph \( G \) from the given list of friendships.
2. **Vertex Degree Calculation**:
   - Calculate the degree of each vertex in the graph.
3. **Isolated and Pendant Vertex Identification**:
   - Identify isolated vertices (students with no friends).
   - Identify pendant vertices (students with exactly one friend).
4. **Graph Visualization**:
   - Visualize the graph using Python.
5. **Interpretation**:
   - Analyze and interpret the graph properties to provide insights into the social network.

## Mathematical Abstraction
- **Graph $\mathbf{G}$**: $\mathbf{G = (V, E)}$, where $\mathbf{V}$ is the set of vertices (students) and \( E \) is the set of edges (friendships).
- **Vertex Degree**: The degree of a vertex \( v \) is the number of edges incident to \( v \).
- **Isolated Vertex**: A vertex with degree 0.
- **Pendant Vertex**: A vertex with degree 1.

## Python Implementation

**Step 1: Graph Representation**
```python
import networkx as nx
import matplotlib.pyplot as plt

# List of friendships (edges)
friendships = [
    (1, 2), (1, 3), (2, 4), (2, 5), (3, 6), (4, 7), (5, 8), (6, 9), (7, 10),
    (8, 11), (9, 12), (10, 13), (11, 14), (12, 15), (13, 16), (14, 17), (15, 18),
    (16, 19), (17, 20), (18, 21), (19, 22), (20, 23), (21, 24), (22, 25), (23, 26),
    (24, 27), (25, 28), (26, 29), (27, 30), (28, 31), (29, 32), (30, 33), (31, 34),
    (32, 35), (33, 1)
]

# Create a graph
G = nx.Graph()
G.add_edges_from(friendships)

# Draw the graph
plt.figure(figsize=(12, 8))
nx.draw(G, with_labels=True, node_color='lightblue', edge_color='gray')
plt.title("Social Network Graph")
plt.savefig("social_network_graph.png")
plt.show()
```
**Step 2: Vertex Degree Calculation**
```python
# Calculate degrees
degrees = dict(G.degree())
print("Degrees:", degrees)
```
**Step 3: Isolated and Pendant Vertex Identification**

```python
# Identify isolated and pendant vertices
isolated_vertices = [v for v, d in degrees.items() if d == 0]
pendant_vertices = [v for v, d in degrees.items() if d == 1]

print("Isolated vertices:", isolated_vertices)
print("Pendant vertices:", pendant_vertices)
```

**Step 4: Graph Visualization**
```python
import networkx as nx
import matplotlib.pyplot as plt

# List of friendships (edges)
friendships = [
    (1, 2), (1, 3), (2, 4), (2, 5), (3, 6), (4, 7), (5, 8), (6, 9), (7, 10),
    (8, 11), (9, 12), (10, 13), (11, 14), (12, 15), (13, 16), (14, 17), (15, 18),
    (16, 19), (17, 20), (18, 21), (19, 22), (20, 23), (21, 24), (22, 25), (23, 26),
    (24, 27), (25, 28), (26, 29), (27, 30), (28, 31), (29, 32), (30, 33), (31, 34),
    (32, 35), (33, 1)
]

# Create a graph
G = nx.Graph()
G.add_edges_from(friendships)

# Draw the graph
plt.figure(figsize=(12, 8))
nx.draw(G, with_labels=True, node_color='lightblue', edge_color='gray')
plt.title("Social Network Graph")
plt.savefig("social_network_graph.png")
plt.show()
```
**Step 5: Interpretation**

1. *Vertex Degree Analysis:*

 - Students with higher degrees are more connected and central to the social network.
 - Students with lower degrees might need social support.
  
2. *Isolated Vertex Analysis:*

 - Isolated vertices represent students with no friends in the network, potentially indicating social isolation.
3. *Pendant Vertex Analysis:*

 - Pendant vertices represent students with only one friend, indicating a limited social circle.

### Conclusion
This DYI project demonstrates the application of basic graph theory concepts to analyze a social network. By representing the network as a graph, calculating vertex degrees, and identifying isolated and pendant vertices, we gain valuable insights into the social dynamics of the student population. This analysis can help the university identify students who might benefit from social interventions and support programs.
