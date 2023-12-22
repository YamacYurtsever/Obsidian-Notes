- A [[Trees | tree]]-like data structure where each node is usually a character of a string
- Particularly useful for problems involving the storage and retrieval of strings
- Can be searched at [[Time Complexity#^fe68a1 | constant time O(1)]] (length of the word being searched), however takes up a lot of memory

![[Pasted image 20231223020142.png | 400]]

#### Implementation
```C
struct Node {
    int value;
    struct Node* children[26]; //English lowercase letters
};
```