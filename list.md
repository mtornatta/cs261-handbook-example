# Lists/Arrays

A **List** is a linear and mutable structure and is the python specific implementation of the **Array** ADT. An array is a linear and mutable structure. Data is stored in an array at an index. This index is then used as a reference to that data and is used to retrieve it from the array.

# In Memory

In memory, a list will look like this:

picture

A list in python will hold a collection of references to information. These references have a memory address associated with them as well as an index to keep track of their position within the list.

# Operations

* **Access:** Gets data stored at a specified position. **O(1)**: a list is ordered and therefore keeps track of where data was entered within it. All it needs to do is perform a calculation to jump to the correct index.
* **Search:** Looks for a piece of data within a list. **O(n)**: a list does not know the data contained at each index so it will have to search itself entirely to find a specific value. This means the search has the potential take longer and longer the larger the list grows.
* **Insert:** Inserts a piece of data after a specified index. **O(n)**: a list can jump to an index easily enough, but after it inserts the information it must then shift all of the data after it over by one index. This will take longer the larger the list is.
* **Delete:** Removes a piece of data at a specified index. **O(n)**: this operation runs into the same pitfalls as insert. It can jump to the data quickly but once it deletes an element it must shift the data after the deleted data over by one the opposite way as inserting.

# Use Cases

A list is useful if you had a lot of information that needed to be indexed so it could be referenced quickly by index number. Lists also come in handy as a base for abstract data types.

Lists run into some problems when you're working with enormous pieces of data and you want to look up a piece of information by the value rather than index or if you are planning to insert and delete information a lot.

# Example

```


```

[Next](set.md)

(c) 2018 Michael Tornatta. All rights reserved.
