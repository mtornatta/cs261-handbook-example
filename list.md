# Lists

A list is an ordered and mutable [collection](collections_overview.md).

# In Memory

In memory, a list will look like this:

picture

A list in python will hold a collection of references to information. These references have a memory address associated with them as well as an index to keep track of their position within the list.

# Operations

A list supports the following operations:

**Core Operations**
* Access: Gets data stored at a specified position. **O(1)**: a list is ordered and therefore keeps track of where data was entered within it. All it needs to do is perform a calculation to jump to the correct index.
* Search: Looks for a piece of data within a list. **O(n)**: a list does not know the data contained at each index so it will have to search itself entirely to find a specific value. This means the search has the potential take longer and longer the larger the list grows.
* Insert: Inserts a piece of data after a specified index. **O(n)**: a list can jump to an index easily enough, but after it inserts the information it must then shift all of the data after it over by one index. This will take longer the larger the list is.
* Delete: Removes a piece of data at a specified index. **O(n)**: this operation runs into the same pitfalls as insert. It can jump to the data quickly but once it deletes an element it must shift the data after the deleted data over by one the opposite way as inserting.

**Structure Specific Operations**
* Append: Adds data after the last item in the list. **O(1)**: a list can append  data in constant time as it keeps track of the last element in the list.
* Pop: Removes data from a specified point and returns that data. **O(1)** when popping from the end of the list. **O(n)** when removing from anywhere else.

# Use Cases

A list is useful if you had a lot of information that needed to be indexed so it could be referenced quickly by index number. Lists also come in handy as a base for abstract data types. 

Lists run into some problems when you're working with enormous pieces of data and you want to look up a piece of information by the value rather than index or if you are planning to insert and delete information a lot.

# Example

```


```

(c) 2018 Michael Tornatta. All rights reserved.
