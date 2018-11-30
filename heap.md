# Binary Heaps

A binary heap is a tree structure and much like the bst the rules by which it organizes itself is what really differentiates it from other trees. For a binary heap to be a binary heap it must fill the levels of the tree from left to right and it must conform to the rules of a **min** or **max** heap. A min heap cannot have a parent larger than its child, that way the minimum value of the heap ends up at the top of the heap. A max heap is the opposite, parents must always be larger than their children. When the value of the parent is not following the rules the node below it will "percolate up" into the position of the parent or "percolate down" into the child position.

# In Memory

In memory, a heap looks like this:

![set image](images/minheap.jpg)

This is an example of a min heap implemented with an array. You can see that an array works well as the underlying structure since heaps are actually ordered. In order to jump to a parent or child you need only perform an operation on the position of the current "node". To get to the left child of a parent you simply have to multiply 2*position of the parent and for the right it's 2*position of the parent + 1. To get to the parent you then perform the opposite operations.

# Operations

* **Search:** Looks for a specific piece of data in a heap. **O(n)**: you have to look through the entire heap to find an element. The time it will take to find an element will be relative to the size of the heap.
* **Add:** Adds data to the heap. **O(log n)**: a new piece of data is added left to right on the lowest level of the heap tree. The rules of the heap must then be followed and the data will percolate to the correct position. This is proportional to the size of the heap but since the heap is still a tree, the problem is cut in half with each percolation making the time logarithmic.
* **Delete:** Removes an element from the heap. **O(log n)**: deletion removes a specified element from the heap then readjusts the heap so it follows its internal rules. Like adding, this is dependent on the size of the heap but the problem is broken into parts due to the tree structure of this ADT.

# Use Cases

A heap is especially useful when you need to know the min or max piece of data in a collection or when you're trying to implement a [priority queue](priority_queue.md).

When you're not looking to find the min or max value you might be better off using a different kind of tree or ADT.

# Example

```

#create a new min heap
test_heap = heap()

#add some elements
heap.add(4)
heap.add(20)
heap.add(14)
#tree now looks like:
#       4
#   20     14

#add a smaller element
heap.add(3)
#3 will percolate up to the top:
#       3
#    4     14
#20

```

[Prev](bst.md) | [Next](priority_queue.md)

[Front Page](README.md)

(c) 2018 Michael Tornatta. All rights reserved.
