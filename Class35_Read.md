 ## Why

Used to represent and analyze relationships between objects or entities. They provide a flexible and efficient way to model complex relationships and solve various problems. 

 ## What

A graph is a collection of nodes (also called vertices) and edges. The nodes represent entities, while the edges represent the relationships between those entities. Graphs can be classified into two main types: directed and undirected. In a directed graph, the edges have a specific direction, while in an undirected graph, the edges have no direction. Graphs can also have weighted edges, where each edge has a value or weight associated with it.

 ## How 

 1. Adjacency Matrix: An adjacency matrix is a two-dimensional matrix where rows and columns represent the nodes of the graph. Each cell in the matrix represents an edge between two nodes. If there is an edge between nodes i and j, the corresponding cell in the matrix is set to 1 (or the weight of the edge if it is a weighted graph). Otherwise, it is set to 0. The adjacency matrix is efficient for dense graphs but requires more space for sparse graphs.

2. Adjacency List: An adjacency list represents a graph as an array of linked lists or arrays. Each node in the array corresponds to a vertex, and its associated list contains the adjacent vertices (or edges) of that vertex. This representation is efficient for sparse graphs as it only requires space proportional to the number of edges. Traversing the adjacency list allows quick access to neighbors of a given node.