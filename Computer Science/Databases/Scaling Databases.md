### Database Partitioning
- Dividing large tables into smaller, more manageable partitions based on certain criteria
- E.g.: Flights -> Flights_Domestic & Flights_International

### Database Replication
- Single Primary Replication
	- One [[Types of Databases | database]] that can be written to and multiple replicas that can be read from
- Multiple Primary Replication
	- Multiple [[Types of Databases | database]] that can be written to and read from
	- Which are all kept in sync through updates

### Caching
- Using an in-memory [[Cache Memory | cache]] to store frequently accessed data and reduce the need for database queries

##### Client-Side Caching
- [[HTTP Requests]] (Cache Related Headers)
```
// Maximum amount of time the resource will stay fresh in seconds
Cache-Control: max-age=86400

// A number sequence that can be used to check with the server if the cached resource has changed
ETag: "769...517"
```

![[Pasted image 20231228133519.png | 550]]

##### Server-Side Caching

![[Pasted image 20231228131615.png | 550]]

### Indexing
- Structures that enhance the speed of retrieval operations (E.g.: SELECT queries) by  reducing the number of rows being searched
- This can result in additional storage space and some overhead during [[Relational Databases#Main Functions of Relational Databases (CRUD) | data modification operations]] (INSERT, UPDATE, DELETE)

```SQL
CREATE INDEX title_index ON shows(title);
```