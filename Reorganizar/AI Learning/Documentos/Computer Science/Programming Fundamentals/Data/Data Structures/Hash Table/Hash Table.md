# Hash Table
A hash table, also known as a hash map, dictionary, or associative array, is a data structure that implements an associative array abstract data type, a structure that can map keys to values. A hash table uses a hash function to compute an index into an array of buckets or slots, from which the desired value can be found.
## Key concepts
Use a `HashMap` when you need to store **key-value pairs** and retrieve values quickly based on their unique keys. You care not just about the presence of an element, but also some associated information with it.
## Advantages
### Fast average-case performance
Insertions, deletion, and lookup operations typically have an average time complexity of O(1).
## Disadvantages
### Performance can degrade in worst-case scenarios
### Not ideal for ordered data
### Implementation complexity
## Maps
A [[Documentos/Computer Science/Programming Fundamentals/Data/Data Structures/Map/Map|Map]] is an abstract data type (ADT), while a hash table is a data structure that can be used to implement a map. So, a hash table is one way to create a map, but not the only way.