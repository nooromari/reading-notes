## Hash table

**Hash table** : is a data structure that implements an associative array abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index into an array of buckets or slots, from which the desired value can be found. *A bucket is what is contained in each index of the array of the hashtable.*

- Ideally, the hash function will assign each key to a unique bucket, but most hash table designs employ an imperfect hash function, which might cause hash collisions where the hash function generates the same index for more than one key.

> In many situations, hash tables turn out to be on average more efficient than search trees or any other table lookup structure. For this reason, they are widely used in many kinds of computer software, particularly for associative arrays, database indexing, caches, and sets.

- Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null we can initialize a `LinkedList` in each one! Now if two keys resolve to the same index in the array then their key/value pairs can be stored as a node in a linked list. 

![](https://yourbasic.org/algorithms/hash-table.png)


- To achieve a good hashing mechanism, It is important to have a good hash function with the following basic requirements:

1. Easy to compute.

2. Uniform distribution.

3. Less collisions.

> Note: Irrespective of how good a hash function is, collisions are bound to occur. Therefore, to maintain the performance of a hash table, it is important to manage collisions through various collision resolution techniques.

- Hash maps take advantage of an array’s `O(1)` read access. Instead of adding elements to an array from beginning to end, a hash map uses a “hash function” to place each item at a precise index location, based off it’s key.



### Internal Methods

- `Add()`

    When adding a new key/value pair to a hashtable:

    send the key to the GetHash method.
    Once you determine the index of where it should be placed, go to that index
    Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
    If something does exist, add the new key/value pair to the data structure within that bucket.

- `Find()`

    The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

- `Contains()`

    The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

- `GetHash()`

    The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.