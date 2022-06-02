# What is Hashtables

Hashtables are a data structure that utilizes key-value pairs. This means every Node or Bucket has both a key and a value. The basic idea of a hashtable is the ability to store the key in this data structure, and quickly retrieve the value. This is done through what we call a hash. A hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

Since we are able to hash our key and determine the exact location where our value is stored, we can do a lookup in an O(1) time complexity. This is ideal when quick lookups are required.

Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.

Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.

Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.




## Hashing is implemented 

An element is converted into an integer by using a hash function. This element can be used as an index to store the original element, which falls into the hash table.

The element is stored in the hash table where it can be quickly retrieved using a hashed key.

hash = hashfunc(key)
index = hash % array_size

## Why do we use them?

- Hold unique values
- Dictionary
- Library

## What Is the Impact of Hash Tables?

Now that we’ve gone over what hash tables are, we can explore how hash tables impact our code. A primary impact of hash tables is their constant time complexity of O(1), meaning that they scale very well when used in algorithms.

Searching over a data structure such as an array presents a linear time complexity of O(n). In other words, as the data structure increases in size, the search time increases in a linear fashion.

Simply put, using a hash table is faster than searching through an array.

In the Find the First Non-Repeating Character algorithm challenge, we use hash tables as an optimal solution compared to nested for loops, which is a reduction in complexity from O(n*n) to O(n).

Another impact of hash tables is that they are excellent for storing paired data. This was my first introduction to hash tables in the form of JavaScript Object Notation (JSON). To me, key-value pairs were an easy way of connecting two fields like { "First Name": "Jonathan" }.

## Internal Methods

- Add 
When adding a new key/value pair to a hashtable:
send the key to the GetHash method.
Once you determine the index of where it should be placed, go to that index
Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
If something does exist, add the new key/value pair to the data structure within that bucket.
Find : 

The Find takes in a key, gets the Hash, and goes to the index location specified. Once the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and sees if the key exists, and return the value.

- Contains

The Contains method will accept a key, and return a bool if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

- GetHash 

The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

