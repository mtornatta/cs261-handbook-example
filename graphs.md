# Graphs

A graph is type of non-linear data structure which can be either directed or undirected. Graphs are comprised of nodes also known as **vertices** and are connected by **edges** which can have **weights** to them.

# In Memory

In memory, a graph looks like this:

![set image](images/graph.jpg)

This type of graph implementation is comprised of vertex objects which hold a value and keep track of their "neighbors" or the vertices adjacent to them and the weights of the edges between neighbors.

# Operations

**Note**: |v| and |e| here mean number of vertices and number of edges in graph, respectively.

* **Search:** Looks for data in a graph. **O(|v|)**: for an adjacency list (which is the type of implementation I'll focus on here, there are others) this operation is dependent on how many vertices there are in the graph. The time it will take to perform this operation will increase as the amount of vertices increases since it has to search the whole graph until it find the specified value.
* **Add Vertex:** Inserts a vertex into the graph **O(1))**: the graph only needs to perform some operations to set references to and from the vertex which only takes a constant amount of time.
* **Remove Vertex:** Removes a vertex from the graph. **O((|v| + |e|)**: this operation is dependent on the amount of vertices and edges since the graph has to traverse the list of vertices and edges until it finds the one to remove.
* **Add Edge:** Adds an edge to the graph **O(1)**: this operation, like adding a vertex, need to perform some operations to create an edge. This happens in constant time regardless of the amount of vertices and edges.
* **Remove Edge:** Removes an edge from the graph. **O(|e|)**: this operation runs into the same pitfalls as removing a vertex. It must search through the list of edges to know what it's deleting.

# Use Cases

A graph has many uses from the purely mathematical to something like linking social media data.

Graphs are useful when needing to connect data and determine the cost of traversing from one piece of data to the next. It's has pretty specific applications and are not as good for random access or prioritizing data.

# Example

```

#create graph (adjacency list implementation)
test_graph = graph()

#assume we've created graph object, lets add some edges (vertex 1, edge weight, vertex 2)
test_graph.addEdge(2,4,20)
test_graph.addEdge(2,5,16)
#note here that you can include the same vertex in multiple edge additions
test_graph.addEdge(16,3,7)

#we've created a graph:
#(2,16) with weight 5
#(2,20) with weight 4
#(16,7) with weight 3

```

[Prev](priority_queue.md) | [Return to Front Page](README.md)

(c) 2018 Michael Tornatta. All rights reserved.
