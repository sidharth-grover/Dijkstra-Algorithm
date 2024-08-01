Repo Link : https://gist.github.com/MagallanesFito/61afb009986f0319774cb079b8914bb2

Includes and Defines

#include <bits/stdc++.h>: Includes most of the standard C++ libraries.
#define INF 0x3f3f3f3f: Defines a large value to represent infinity (INF).
using namespace std: Uses the standard namespace.
typedef pair<int,int> myPair: Defines a type alias myPair for pair<int, int>.

Graph Class Definition

Graph: A class representing a graph.
int V: Number of vertices.
list<myPair> *adj: Pointer to an array of adjacency lists.

Constructor

Graph::Graph(int V): Constructor that initializes the graph with V vertices and creates an array of adjacency lists.

addEdge Function

void Graph::addEdge(int u, int v, int w): Adds an edge to the graph.
u: Start vertex.
v: End vertex.
w: Weight of the edge.
Adds an edge from u to v with weight w and from v to u with weight w.

shortestPath Function

void Graph::shortestPath(int src): Implements Dijkstra's algorithm to find the shortest paths from a source vertex src.
Uses a priority queue pq to pick the minimum distance vertex.
Initializes a distance vector dist with all distances as infinity (INF) and sets the distance to the source vertex as 0.
The main loop extracts the vertex with the minimum distance, updates the distance of its adjacent vertices, and pushes them to the priority queue if a shorter path is found.
After the main loop, it prints the shortest distances from the source vertex to all other vertices.

Main Function

int main(): The entry point of the program.
Creates a graph g with 5 vertices.
Commented out section to add edges (replace a, b, and w with actual values to add edges).
Calls shortestPath with source vertex src = 0.
Returns 0 to indicate successful execution.
