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