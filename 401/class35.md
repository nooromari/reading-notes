## Graphs

A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.


Common terminology used when working with Graphs:

| Term | Definition |
|--|--|
| Vertex | is a data object that can have zero or more adjacent vertices. Also called a “node”. |
| Edge | is a connection between two nodes. |
| Neighbor | The neighbors of a node are its adjacent nodes, i.e., are connected via an edge. |
| Degree | The degree of a vertex is the number of edges connected to that vertex. |


### Directed vs Undirected


- **Undirected Graphs**: is a graph where each edge is undirected or bi-directional.


- **Directed Graphs (Digraph)**: is a graph where every edge is directed.

![](https://i.imgur.com/JWL96oK.png)


### Complete vs Connected vs Disconnected

- **Complete Graphs**: A complete graph is when all nodes are connected to all other nodes.

![](https://d2r55xnwy6nx47.cloudfront.net/uploads/2020/02/Ringels_Figs01.jpg)

- **Connected**: A connected graph is graph that has all of vertices(nodes) have at least one edge.

*A Tree is a form of a connected grap*

- **Disconnected**: A disconnected graph is a graph where some vertices may not have edges.

![](https://i0.wp.com/algorithms.tutorialhorizon.com/files/2019/10/Connected-Undirected-Graph-Example.png?resize=967%2C397&ssl=1)


### Acyclic vs Cyclic

- **Acyclic Graph**: An acyclic graph is a directed graph without cycles.

*A cycle is when a node can be traversed through and potentially end up back at itself.*

- **Cyclic Graphs**: A Cyclic graph is a graph that has cycles.

*A directed acyclic graph is also called a DAG. This can also be represented as what we know as a tree.*

![](https://apprize.best/php/hadoop_1/hadoop_1.files/image190.jpg)


### Graph Representation:

1. **Adjacency Matrix**

![](https://static.javatpoint.com/ds/images/sequential-representation.png)

1. **Adjacency List**

![](https://i.imgur.com/ylcZpyH.jpg)

### Weighted Graphs

A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights.

![](https://static.javatpoint.com/ds/images/sequential-representation3.png)

![](https://i.imgur.com/ylcZpyH.jpg)


Graphs are extremely popular when it comes to it's uses. Here are just
a few examples of graphs in use:

1. GPS and Mapping
1. Driving Directions
1. Social Networks
1. Airline Traffic
1. Netflix uses graphs for suggestions of products
