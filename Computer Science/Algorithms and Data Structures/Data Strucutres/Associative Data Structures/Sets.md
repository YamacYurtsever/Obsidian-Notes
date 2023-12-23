- Represent a collection of distinct elements, where the order of the elements is typically not significant
- The primary characteristic of a set is that it does not allow duplicate elements, ensuring that each element is unique within the collection

#### Key Operations
- Creating Sets
```python
set1 = {1, 2, 3, 4, 5}
set2 = {3, 4, 5, 6, 7}
```
- Union
```python
union_set = set1 | set2
union_set = set1.union(set2)
```
- Intersection
```python
intersection_set = set1 & set2
intersection_set = set1.intersection(set2)
```
- Difference
```python
difference_set = set1 - set2
difference_set = set1.difference(set2)
```
- Subset
```python
is_subset = set1 <= set2
is_subset = set1.issubset(set2)
```
- Superset
```python
is_superset = set1 >= set2
is_superset = set1.issuperset(set2)`
```
- Adding
```python
set1.add(6)
```
- Removing
```python
set1.remove(3)
```
