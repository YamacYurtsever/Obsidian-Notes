- Structures that enhance the speed of retrieval operations (E.g.: SELECT queries) by  reducing the number of rows being searched
- This can result in additional storage space and some overhead during [[Relational Databases#Main Functions of Relational Databases (CRUD) | data modification operations]] (INSERT, UPDATE, DELETE)

```SQL
CREATE INDEX title_index ON shows(title);
```