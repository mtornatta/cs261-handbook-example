# Hash Tables

A hash table is a structure containing pieces of data mapped to a key using a **hash function**. The key is used to store and access the data within the hash table.

# In Memory

In memory, a hash table looks like this:

![set image](images/hashtable.jpg)

A hash table like this, implemented with arrays, will start out with a set capacity or number of "slots" in which it can hash data to. The structure also keeps track of keys which map to a corresponding piece of data using a hash funciton.

# Operations

* **Get:** Get retrieves specified date from the hash table. **O(1)**: hash tables only need to perform a hashing function which is a set of operations, so it performs at constant time.
* **Search:** Looks for a piece of data within a hash table. **O(1)**: since hash tables work by mapping data using hashing functions, you just need to solve for the hashing function when set to the desired output in order to see if the value exists in the collection.
* **Put:** Enters a piece of data and it's corresponding key into the hash table. **O(1)**: entering data is just as easy as retrieving data in a hash table. It's performed through a hashing function and is therefore always performing at a constant time.
* **Delete:** Removes a piece of data from the hash table. **O(1)**: deleting uses the same methods as all of the other operations and requires the use of the hashing function to locate the data to be removed and then remove it. Again, since this relies on a set of operations within the hashing function it performs at a constant speed.

# Use Cases

Hash tables are really helpful when you're wanting to store and retrieve data from huge collections of data quickly. Hash tables also really excel at checking if a piece of data exists within the structure.

Hash tables have a lot of awesome applications but don't do well when data is not easily hashable (like in an object with no clear surface value) or if you needed to compare two sets of data to each other (with a hash table it would be somewhat difficult to compare its elements to that of another hash table's).

# Example

```

#initialize a hash table, will be created with a default amount of slots
test_hash = hashtable()

#maps a value 33 to the key 1
test_hash.put(1,33)

#retrieve 33 through the use of its key
test_hash.get(1)

```

[Prev](deque.md) | [Next](trees_overview.md)

[Front Page](README.md)

(c) 2018 Michael Tornatta. All rights reserved.
