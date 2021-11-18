# Hash Tables

+ Hashtables : data structure that utilize key value pairs. 

+ Hash : is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose.

+ Buckets : is what is contained in each index of the array of the hashtable. Each index is a bucket. 

+ Collisions : is what happens when more than one key gets hashed to the same location of the hashtable.


+ we use them for hold unique values ,dictionary and library

![](https://www.bogotobogo.com/Algorithms/images/hash_table/open_addressing.png)


+ Hash maps do this to store values:

  + accept a key
   
  + calculate the hash of the key

  + use modulus to convert the hash into an array index
  store the key with the value by appending both to the end of a linked list

+ Hash maps do this to read value:

  + accept a key
   
  + calculate the hash of the key

  + use modulus to convert the hash into an array index
  use the array index to access the short LinkedList representing a bucket

  + search through the bucket looking for a node with a key/value pair that matches the key you were given