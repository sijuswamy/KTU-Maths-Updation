## $\color{blue}{\text{GAMAT401- Mathematics for Computer and Information Science}}$

----
### Course Overview
Graph Theory is a fundamental area of study in computer science engineering, providing essential tools for modeling and solving problems in various domains such as network design, social network analysis, and optimization problems. This course aims to introduce students to the key concepts, algorithms, and applications of graph theory with a focus on its practical relevance to computer science.

----

## Syllabus

**Module 1:** Introduction to Graphs - Basic definition, Application of graphs, finite and infinite graphs, Incidence and Degree, Order, Isolated vertex, pendant vertex and Null graph, Degree sequence, Havel-Hakimi Theorem.  Isomorphism, sub graphs, walks, paths and circuits, connected graphs, disconnected graphs and component.

**Module 2:** Euler graphs, Operations on Graphs, Hamiltonian paths and circuits, Travelling Salesman Problem, ,connectivity ,edge connectivity, vertex connectivity, directed graphs ,types of directed graphs.

**Module 3:** Trees — properties, pendant vertex, Distance and centres in a tree - Rooted and binary trees, counting trees, spanning trees, Prim's algorithm and Kruskal's algorithm, Dijkstra's shortest path algorithm, Floyd-Warshall shortest path algorithm.

**Module 4:** Matrix representation of graphs- Adjacency matrix, Incidence Matrix, Circuit Matrix, Path Matrix. Coloring- Chromatic number, Chromatic polynomial,. Greedy colouring algorithm- Four colour theorem, Five colour theorem.

##  Course Design Philosophy

This course is designed as the gateway to Knowledge representation and Network analysis. As it is an introductory course, it is a breadth course for the Computer Science & Engineering and Allied programs.

## $\color{red}{\text{Instructional Design for Teaching Graph Theory}}$

## Theme
The instructional design for teaching graph theory to computer science engineering students aims to provide a comprehensive understanding of both abstract and practical aspects of graph theory. Each concept will be introduced with an example, followed by abstraction, practice problems (both theoretical and applied), and computational implementation. This approach ensures that students grasp the theoretical underpinnings and develop algorithmic thinking and computational skills essential for their professional growth.

## Teaching Paradigm
### Abstract and Practical Viewpoints
Graph theory concepts are presented in a manner that balances abstract mathematical foundations with practical applications. This dual approach helps students understand the relevance of graph theory in solving real-world problems.

### Example-Driven Learning
Each concept is introduced with a concrete example to help students visualize and understand the idea before diving into formal definitions and theoretical aspects. This contextual learning aids in better comprehension and retention.

### Abstraction
Following the example, the concept is abstracted into formal mathematical definitions and properties. This step solidifies the students' understanding and prepares them for more complex applications and problems.

### Practice Problems
#### Formative Assessments (Pen and Paper)
Students practice abstract and application-level problems using traditional methods, focusing on formative assessments to reinforce learning. This step includes drawing graphs, identifying properties, and solving theoretical problems.

#### Computational Approach (Algorithmic Thinking)
Students implement the concepts in Python, developing their computational and algorithmic thinking skills. This hands-on practice bridges the gap between theory and practical application, preparing students for real-world challenges.

### Session Structure
1. **Introduction**
   - Brief overview of the session's topic.
   - Relevance of the concept in computer science and real-world applications.

2. **Presentation of Concepts and Methodologies**
   - Introduction of the concept with a concrete example.
   - Formal definitions and theoretical abstraction.
   - Discussion of properties and methodologies.

3. **Problem Solving**
   - Practice problems (pen and paper) for formative assessment.
   - Computational problems to develop algorithmic thinking.
   - Real-world application problems to demonstrate practical relevance.

4. **Key Takeaway and Conclusion**
   - Summary of the key concepts learned in the session.
   - Discussion on the importance and future applications of the concepts.
   - Reflection on the learning outcomes and preparation for upcoming topics.


## Example Session: Graph Definition and Terminologies
A sample session explaining the new approach in lesson planing is shown [here](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/GAMAT401_Sample_Lesson.md)

## Course Delivery Guidelines

### Module 1: Elements of Graph Theory (8 hours)

- Introduce the fundamentals of graph theory in a application view point (refer [sample lesson](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/GAMAT401_Sample_Lesson.md)).
- Introduce the Havel-Hakimi theorem with a practical application in verifying if a given social network's degree sequence is graphical to ensure feasible network construction.
- Introduce the concept of graph isomorphism with a practical application in determining if two different network structures represent the same social network to ensure consistent analysis and optimization.
- Introduce subgraphs, walks, paths, and circuits with a practical application in analyzing different routes and connections within a transportation network (or use a practical application in analyzing network routing and connectivity within a computer network).
- Introduce connected and disconnected graphs with a practical application in evaluating the robustness and resilience of computer network topologies.
- Introduce graph components with a practical application in identifying isolated communities within a larger social network (or  with a practical application in identifying isolated sub-networks within a larger computer network).
- **Micro Project:** Assessing Network Fault Tolerance and Connectivity Using Graph Theory Techniques.
  >*Problem statement and Definition:*
  
  -- Problem Statement: "Evaluate the connectivity and fault tolerance of a computer network by identifying critical components and analyzing the impact of potential network disconnections on overall network robustness."
  
 --Definition: In this micro project, you will model a computer network as a graph where nodes represent network devices (e.g., routers, switches) and edges represent the connections between these devices. Using graph theory concepts, you will analyze the network’s connectivity, identify critical components, and assess how potential disconnections affect network reliability.
 >*Expected Deliverables:* With proper assumptions, variables and dataset provide the following in the report.
1. Network Graph Visualization: A visual representation of the computer network.
2. Degree Sequence Analysis: Results from applying the Havel-Hakimi theorem.
3. Isomorphism Report: Analysis of isomorphism between network configurations.
4. Subgraph and Path Analysis: Visualization and interpretation of subgraphs, paths, and cycles.
5. Connectivity Report: Assessment of connected and disconnected components.
6. Fault Tolerance Analysis: Evaluation of isolated components and their impact on network reliability.

## Module 2: Reachability and Connectivity Using Graph Models (9 hours)

- Introduce connectivity in network graphs by explaining how to determine if a graph is connected or not with proper example
- Introduce edge connectivity in network graphs by demonstrating how to determine the minimum number of edges that need to be removed to disconnect the graph (recommend the network robustness analysis as example).
- Introduce vertex connectivity by determining the minimum number of vertices whose removal disconnects the graph and evaluating its impact on network robustness.
- Introduce directed graphs by exploring how edges with direction affect connectivity and flow in a network, using examples like traffic routing or email chains to illustrate the concepts.
- Introduce types of directed graphs by exploring examples like Directed Acyclic Graphs (DAGs) for scheduling, strongly connected graphs for web link analysis, and weakly connected graphs for social networks.
- Introduce Euler graphs by examining graphs that contain an Eulerian circuit or path, using examples like routing problems where every edge must be traversed exactly once.
- Introduce operations on graphs by exploring fundamental manipulations, using practical examples like network design and optimization.
- Introduce Hamiltonian paths and circuits by examining examples like finding a route that visits each city exactly once (Hamiltonian path) or returns to the starting city (Hamiltonian circuit) in a network.
- Introduce the Traveling Salesman Problem (TSP), using examples from logistics and route optimization.
- compare different connectivities with special types of graphs like Euler graphs, Hamiltonian graphs, and directed graphs to highlight their unique traversal and  properties.

**Micro project:** Analyzing Epidemic Spread Using Graph Theory

>*Problem Statement:*Model and analyze the spread of an epidemic in a network where nodes represent individuals and edges represent interactions. Evaluate network connectivity, simulate epidemic spread, and assess graph properties to understand and control the epidemic.
>*Expected Deliverables:*

1. Network Graph Visualization: Images of the population network showing nodes and edges.
2. Connectivity Report: Analysis of network connectivity and connected components.
3. Epidemic Spread Simulation Results: Data showing infection spread over steps.
4. Eulerian and Hamiltonian Path/Circuit Analysis: Report on the existence of Eulerian and Hamiltonian paths/circuits.
5. Connectivity Metrics: Values for edge and vertex connectivity.
6. Shortest Path Analysis: Shortest path between specified nodes.(need to be use additional tools for this task)
7. Reachability Results: Nodes reachable from selected starting points.

## Module 3: Trees (10 hours)

- Introduce a tree with the example of a family tree, where each person is a node and family relationships are edges, ensuring a unique path between any two individuals.
- Introduce pendant vertices as endpoints of transmission lines, distance as the number of line segments between two substations, and centers as the optimal substations minimizing the maximum distance to all other substations in a power grid.
- Introduce rooted trees as hierarchical structures with a designated root node and binary trees as a type of rooted tree where each node has at most two children, using the example of a restricted file directory where the root is the top-level folder and each folder can contain up to two subfolders.
- Introduce counting trees, using the example of different hierarchical structures that can be created for a team of employees reporting to a single manager.
- Introduce spanning trees with the example of finding the minimum cabling needed to connect all computers in a network.
- Introduce Prim's algorithm with the example of finding the minimum cost to connect all cities in the National Highway network with the least total road length.
- Introduce Kruskal's algorithm with the example of finding the minimum cost to connect all cities by considering the shortest roads between them.
- Introduce the comparison of Prim's and Kruskal's algorithms with the example of finding the minimum cost to connect all cities: Prim's algorithm grows the network from a starting city, while Kruskal's algorithm sorts and connects the shortest roads between any cities.
- Introduce Dijkstra's shortest path algorithm with the example of finding the shortest route from *one city to another* in a network, minimizing travel distance or time.
- Introduce the Floyd-Warshall shortest path algorithm with the example of finding the shortest paths between all pairs of cities in a network, comparing it to Dijkstra’s algorithm, which finds the shortest path from a single source to a specific destination.

**Micro Project** Network Optimization for a Smart City (Data driven)
>*Problem Statement:*
Design and optimize a smart city network to ensure efficient connectivity between critical infrastructure elements such as data centers, power plants, emergency services, and public facilities given in the dataset [nodes.csv](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/nodes.csv), [edges.csv](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/edges.csv). The goal is to minimize infrastructure costs, improve response times, and ensure robust communication pathways.
>*Expected deliverables:*
1. Network Design: Create a graph model representing a smart city network using data from CSV files.
2. Minimum Spanning Tree: Apply Prim’s and Kruskal’s algorithms to identify the least-cost network connections while ensuring all essential nodes are connected.
3. Shortest Path Calculation: Utilize Dijkstra's and Floyd-Warshall algorithms to find the shortest communication paths between nodes.
4. Network Analysis: Assess connectivity, identify key network nodes (pendant vertices and centers), and ensure optimal performance.
5. Recommendations based on the analysis for improving network connectivity, minimizing costs, and enhancing performance. This will include suggestions for network upgrades or restructuring to ensure robust and efficient communication pathways.

## Module 4: Matrix Representation of Graphs

- Introduce the concept of adjacency matrices using the example of a small network of three computers connected in a triangle to visualize and analyze their connections.
- Introduce the concept of incidence matrices using the example of a small social network of four friends, where each connection represents a friendship, to visualize and analyze their relationships.
- Introduce the concept of circuit matrices using the example of a road network with *three distinct routes connecting intersections* to visualize and analyze their connections.
- Introduce the concept of path matrices using the example of a small city road network with *four intersections* to visualize and analyze the possible routes between intersections.
- Introduce the concept of the chromatic number using the example of a map with four neighboring countries to visualize and determine the minimum number of colors needed to ensure no two adjacent countries share the same color.
- Introduce the concept of the chromatic polynomial using the previous example of a map.
- Introduce the concept of the greedy coloring algorithm using the example of a map using a simple, step-by-step approach.
- Introduce the Five Color Theorem and discuss its application in optimizing aircraft scheduling to ensure no two flights with conflicting schedules are assigned the same gate or runway (application can be given as an assignment).
- Introduce the Four Color Theorem and discuss its use in optimizing resource allocation by minimizing the number of resources needed to ensure no conflicts (application can be given as an assignment).

**Micro Project:** Advanced Resource Allocation Optimization in a Large Institution with Graph Theory Techniques (Comprehensive Project)

>*Objective:* Utilize advanced graph theory concepts to design, analyze, and optimize resource allocation in a large institution with a focus on efficient management of classrooms, laboratories, and scheduling using the dataset [resourses.csv](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/resources.csv), [courses.csv](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/courses.csv), [constraints.csv](https://github.com/sijuswamy/KTU-Maths-Updation/blob/main/constraints.csv).
>
>*Problem Statement:* Design and optimize the resource allocation and scheduling system for an institution with multiple courses, including a substantial number of classrooms and laboratories. Represent the resources and scheduling constraints as a graph. Apply graph theory techniques to ensure efficient allocation and minimize conflicts.

>*Expected Deliverables:*

1. Graph Construction and Visualization:

 - Construct and visualize the network graph representing courses, classrooms, and laboratories.
 - Generate and analyze adjacency and incidence matrices to understand connections between resources.
 - Resource Allocation and Coloring:

2. Apply greedy coloring algorithms and compute the chromatic number to allocate resources such as classrooms and labs efficiently.
   
 - Analyze and compare greedy and exact coloring methods.
 - Pathfinding and Optimization: Use Dijkstra’s and Floyd-Warshall algorithms to find shortest paths and optimize routes between resources.
   
4. Advanced Analysis:

 - Compute circuit matrices and path matrices to analyze the network's connectivity and identify potential scheduling conflicts.
 - Apply advanced graph algorithms to solve scheduling and resource allocation problems.
5. Optimization Report: Provide a comprehensive report detailing findings, optimization strategies, and recommendations based on graph theory analysis.
