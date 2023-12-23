- Hash tables (also known as dictionaries, maps, hashes) are data structures that implement an associative array, a structure that can map keys to value
- It is designed for efficient insertion, deletion, and retrieval of data based on keys
- The primary idea behind a hash table is to use a hash function to compute an index into an array of buckets or slots, from which the desired value can be found
- Normally hash tables can be searched at [[Time Complexity#^fe68a1 | constant time O(1)]], however if many keys hash to the same index, then the time complexity may degrade to [[Time Complexity#^2171dc | linear time O(n)]]
- The efficiency of a hash table is associated with a balanced distribution of elements across its indices

![[Hash Tables 2023-12-23 13.09.27.excalidraw]]

#### Hash Function
- The hash function takes a key as input and produces a fixed-size hash code or hash value
- The hash code is used to determine the index of the array where the corresponding value will be stored or looked up.

#### Collision Handling
- Collisions occur when two keys hash to the same index.
- Hash tables employ various collision resolution techniques to handle this, such as:
	- **Chaining**: Each bucket contains a linked list of key-value pairs that hash to the same index.
	- **Open Addressing**: The collision resolution involves searching for the next available slot in the array.

#### Implementation
C
```C
typedef struct KeyValue {
    char *key;
    int value;
    struct KeyValue *next;
} KeyValue;

typedef struct HashTable {
    int size;
    KeyValue **table;
} HashTable;
```

Python (Dictionaries)
```python
my_dict = {'name': 'John', 'age': 25, 'city': 'New York'}

my_dict['gender'] = 'Male'

my_dict['age'] = 26

del my_dict['city']

if 'name' in my_dict:
    print(f"Name: {my_dict['name']}")
```
