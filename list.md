# Lists/Arrays

A **List** is a linear and mutable structure and is the python specific implementation of the **Array** ADT. An array is a linear and mutable structure. Data is stored in an array at an index. This index is then used as a reference to that data and is used to retrieve it from the array.

# In Memory

In memory, a list will look like this:

![array image](images/array.jpg)

A list/array structure contains pieces of data which are stored at a memory address (note that all of the array's assigned memory addresses have some sort of order to them) and are accessed by an index which references the data.

# Operations

* **Access:** Gets data stored at a specified position. **O(1)**: a list is ordered and therefore keeps track of where data was entered within it. All it needs to do is perform a calculation to jump to the correct index.
* **Search:** Looks for a piece of data within a list. **O(n)**: a list does not know the data contained at each index so it will have to search itself entirely to find a specific value. This means the search has the potential take longer and longer the larger the list grows.
* **Insert:** Inserts a piece of data after a specified index. **O(n)**: a list can jump to an index easily enough, but after it inserts the information it must then shift all of the data after it over by one index. This will take longer the larger the list is.
* **Remove:** Removes a piece of data at a specified index. **O(n)**: this operation runs into the same pitfalls as insert. It can jump to the data quickly but once it deletes an element it must shift the data after the deleted data over by one the opposite way as inserting.

# Use Cases

A list is useful if you had a lot of information that needed to be indexed so it could be referenced quickly by index number. Lists also come in handy as a base for abstract data types.

Lists run into some problems when you're working with enormous pieces of data and you want to look up a piece of information by the value rather than index or if you are planning to insert and delete information a lot.

# Example

```
#create a list/array
test_list = [1,24,55,69]

#set a value at an index
test_list[3] = [6]
#the value stored at index 3 has now been set from 69 to 6

#appending will add an item to the end of the list
test_list.append(27)

```

[Prev](basic_adt_overview.md) | [Next](set.md)

[Front Page](README.md)

(c) 2018 Michael Tornatta. All rights reserved.
