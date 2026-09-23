# Database Design Notes

## Relational Database Management System (RDBMS)

### Scaling Techniques

#### Master-Slave Replication
- Writes go to master, reads go to slaves
- Improves read throughput
- Risk: Replication lag, slave failure

#### Master-Master Replication
- Both masters accept writes
- Higher availability
- Risk: Conflicts, synchronization issues

#### Federation
- Split databases by function (e.g., users, orders, products)
- Reduces load on individual databases
- Adds complexity to queries

#### Sharding
- Split data across multiple databases by a shard key
- Horizontal partitioning
- Challenge: Choosing the right shard key, cross-shard queries

#### Denormalization
- Add redundant data to avoid joins
- Improves read performance
- Increases storage and write complexity

#### SQL Tuning
- Proper indexing
- Query optimization
- Connection pooling

### Key Takeaways
- Vertical scaling = bigger server (limited)
- Horizontal scaling = more servers (complex but unlimited)
- Replication = read scaling
- Sharding = write scaling

## NoSQL Databases

### Key-Value Store
- **Abstraction**: Hash table
- **Operations**: O(1) reads/writes
- **Use cases**: Caching, session storage, simple data
- **Examples**: Redis, Memcached, DynamoDB
- **Trade-off**: Limited query capabilities

### Document Store
- **Abstraction**: Key-value store with documents as values
- **Structure**: JSON/XML documents, collections
- **Use cases**: Content management, catalogs, user profiles
- **Examples**: MongoDB, CouchDB, Elasticsearch
- **Trade-off**: Document size limits, eventual consistency

### Wide Column Store
- **Abstraction**: Nested map `ColumnFamily<RowKey, Columns<ColKey, Value, Timestamp>>`
- **Use cases**: Large datasets, time-series data
- **Examples**: Cassandra, HBase, Bigtable
- **Trade-off**: Complex data model, eventual consistency

### Graph Database
- **Abstraction**: Graph (nodes and edges)
- **Use cases**: Social networks, recommendation engines
- **Examples**: Neo4j, FlockDB
- **Trade-off**: Not widely adopted, harder to find tools

## SQL or NoSQL?

**Choose SQL when:**
- Need ACID transactions
- Data is structured and normalized
- Complex joins required
- Strong consistency needed

**Choose NoSQL when:**
- Schema evolves frequently
- Need to scale horizontally
- Simple data model
- Eventual consistency is acceptable
- High write throughput needed

## Node.js Developer Notes

- **MongoDB**: Document store, great with Node.js JSON-like data
- **PostgreSQL**: RDBMS, ACID compliant, good for financial data
- **Redis**: Key-value store, excellent for caching and sessions
- **Connection pooling**: Use `pg-pool` or `mongoose` connection pooling
- **ORMs**: Sequelize (SQL), Mongoose (MongoDB) - but understand what they abstract away

## Sources
- [SQL vs NoSQL decision guide](https://www.infoq.com/articles/Transition-RDBMS-NoSQL/)
- [NoSQL patterns](http://horicky.blogspot.com/2009/11/nosql-patterns.html)
