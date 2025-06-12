# CSCI-3110-Project-8-From-Here-to-Everywhere-solution

Download Here: [CSCI 3110 Project 8: From Here to Everywhere solution](https://jarviscodinghub.com/assignment/project-8-from-here-to-everywhere-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

File(s) to be submitted: proj8.cpp, graph.h, graph.cpp, makefile
Above files must be uploaded individually.
Submit only above files. DO NOT submit a zip file.

Objectives: 1) Implement graphs and graph algorithms; 2) Use STL sets.

Overview:
Write a class that implements a graph and determines the single source shortest paths. Both undirected and
directed graphs must be supported.

Project description:
The program should have a class that implements a graph, consisting of distinct vertices and edges, and constructors for
graphs and edges. Its primary function is Dijkstra’s algorithm for determining the shortest paths from any vertex. The
implementation must use STL sets of pairs to store vertices for calculating the single-source shortest path.

Requirements:
1. Your program must be split into 3 files. There will be a class (with separate interface and implementation files), and a
client/driver file.

The requirements for these are specified below:
a) The Graph class – This class represents a graph and operations on graphs
 Files must be named graph.h and graph.cpp
 Class must be named Graph
 The interface (header file) is provided.

o You should implement the interface file in a .cpp implementation file
o All data members must be of the type specified in the header file
o All member functions in the interface file must be implemented as declared – However you have
flexibility in how you choose to implement each, without changing function prototypes/signatures.

o The graph is to be represented using the adjacency list declared in the header file.
o Use std::numeric_limits::infinity() to set initial path costs to infinity (must #include )
 In addition to the constructor, the following functions are part of the Graph class:
o addEdge(int startvertex, int endverrtex, double weight, bool directed) – This function accepts
information on an edge, and adds its (complete) representation to the adjacency list. Output
information on the edge as it is added to the list (see sample below)

o DijkstraPaths(int vertex) – This function determines the single-source shortest path for all vertices
in the graph, beginning with the vertex specified as the argument. It must use a set, to store the
cost-so-far for vertices as they’re discovered (open list). The output for each vertex is its number
(zero-based), its total cost from the source vertex, and its preceding vertex (through which the
shortest path is obtained). For the source (first) vertex, the preceding vertex is shown as -1. See
sample output below.

b) A driver, or client, file that
 Must be named proj8.cpp
 Reads an input file named graph.txt that contains a graph: the graph may be undirected, or it may be
directed (your code must handle both).

It is represented in the file by:
o A header line containing three (3) integers: The first integer is the number of vertices in the graph
(minimum of 3 vertices for each graph); the second is the number of edge records that follow the
header line; the third is the starting vertex for the single source shortest paths computation.

o Each edge record consists of: two integers representing a “From” vertex and a “To” vertex; a double
for the edge’s weight or cost; and a string with either value “true” or value “false” (case sensitive)
that indicates whether the edge is directed (true) or not (false).

o Note the following regarding edge records:
 Vertices are numbered from 0 to number of vertices minus 1.
 Directed edge records begin with “From” vertex, and present each “To” vertex in order for
each vertex: all edges (if any) from vertex 0 to other vertices are presented in order, then all
edges (if any) from vertex 1 to other vertices in order, etc. See sample file.

 Undirected edges are only presented once. An edge between vertex 1 and vertex 3 is
shown once (even though its representation must be bidirectional).
Ex: an undirected edge between vertex 0 and vertex 2 with weight 5.7 will be stored as:
0 2 5.7 false
Ex: a directed edge from vertex 2 to vertex 6 with weight 4.1 will be stored as:
2 6 4.1 true
 Instantiate the graph object by invoking the single argument constructor (with the number of vertices).
 Call addEdge once for each edge read from the file
 Invoke DijkstraPaths with the starting vertex read from the file.

2. Sample output:
The below output shows program execution on two graphs. The graphs used for this sample output are provided as
a testing aid in file samplegraphs.txt – Note these must be copied individually to the graph.txt file for testing.
This is a directed graph (shortest paths from vertex 3). This is an undirected graph (shortest paths from vertex 2).

3. Test your program – Use multiple graph types and different starting vertices to test your program.

4. Code comments – Add the following comments to your code:
 A section at the top of the source file(s) with the following identifying information:
Your Name
CSCI 3110-00X (your section #)
Project #X
Due: mm/dd/yy

 Below your name add comments in each file that give an overview of the program or class.
 Place a one or two line comment above each function that summarizes the workings of the function.

5. Rubric
Requirements Points Off
Graph: Has constructor that accepts an int (number of vertices) -5
Graph: addEdge: Implemented as declared in the specifications/header file -10
Graph: addEdge: Adds edge to graph using adjacency list representation -10
Graph: addEdge: Outputs the edge’s from and to vertices, along with its weight upon adding it -5
Graph: DijkstraPaths: Implemented as declared in the specifications/header file -10
Graph: DijkstraPaths: Initializes costs to infinity -5

Graph: DijkstraPaths: Uses a std::set of std::pair to store unprocessed vertices (the open list) -10
Graph: DijkstraPaths: Computes the single source shortest path to every vertex -15
Graph: DijkstraPaths: Outputs the shortest paths for all vertices -10
main: Input filename as specified -5
main: Data correctly read from file -10

main: Instantiate Graph object using the single argument constructor (with number of vertices) -5
main: Call addEdge for each edge in the graph file -5
main: Invoke DijkstraPaths with the starting vertex read from the file -5
main: Output closely matches specification (perfect spacing not required) -5
general: Does not compile (on ranger using Linux g++ compiler, and the provided makefile) -25
general: Runtime crash -25
general: Other TBD

