- Immutable collections of data, meaning their values cannot be changed once they are assigned, and they can not be inserted into or deleted from
- This immutability makes tuples useful in situations where you want to ensure that the data remains constant throughout its lifecycle
- **Has a fixed size** and can contain **different data types**
- Can be searched at [[Time Complexity#^2171dc | linear time O(n)]]

#### Implementation
```python
myTuple = (8, "Maximillian", 'g')
name = myTuple[1]
myTuple[0] = 7; #ERROR
```