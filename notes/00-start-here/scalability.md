# Scalability & System Design Fundamentals

## What is System Design?

System design is the process of defining the architecture, components, modules, interfaces, and data for a system to satisfy specified requirements.

## Why System Design Matters for Node.js Developers

You've built APIs and deployed full-stack projects on VPS. System design takes you from "it works on my server" to "it works for millions of users."

## Step 1: Review the Scalability Video Lecture

**[Scalability Lecture at Harvard](https://www.youtube.com/watch?v=-W9F__D3oY4)**

Topics covered:
- Vertical scaling
- Horizontal scaling
- Caching
- Load balancing
- Database replication
- Database partitioning

## Step 2: Review the Scalability Article

**[Scalability by lecloud.net](https://web.archive.org/web/20221030091841/http://www.lecloud.net/tagged/scalability/chrono)**

- Part 1: Clones (horizontal scaling)
- Part 2: Databases (replication, partitioning)
- Part 3: Caches
- Part 4: Asynchronism

## Key Concepts

### Performance vs Scalability

| | Performance Problem | Scalability Problem |
|---|---|---|
| **Definition** | System is slow for a single user | System is fast for one user but slow under load |
| **Analogy** | Car is slow | Highway is congested |
| **Fix** | Optimize code/hardware | Add more servers |

### Latency vs Throughput

- **Latency**: Time to perform some action
- **Throughput**: Number of actions per unit of time
- **Goal**: Maximal throughput with acceptable latency

### Availability vs Consistency (CAP Theorem)

In a distributed system, you can only support **2 of 3**:
- **Consistency**: Every read gets the most recent write
- **Availability**: Every request gets a response
- **Partition Tolerance**: System works despite network failures

**Networks aren't reliable → You need partition tolerance**
→ Trade-off between consistency and availability

#### CP (Consistency + Partition Tolerance)
- Good for: Atomic reads/writes
- Example: RDBMS, HBase
- Risk: Timeout errors during partitions

#### AP (Availability + Partition Tolerance)
- Good for: Highly available systems, eventual consistency
- Example: DNS, email, Cassandra
- Risk: Stale data during partitions

## Consistency Patterns

| Pattern | Description | Use Case |
|---|---|---|
| **Weak consistency** | Reads may or may not see a write | VoIP, video chat, gaming |
| **Eventual consistency** | Reads eventually see writes (ms) | DNS, email, social feeds |
| **Strong consistency** | Reads always see the latest write | Financial transactions, RDBMS |

## Availability Patterns

- **Fail-over**: Switch to backup when primary fails
- **Replication**: Multiple copies of data
  - Master-slave
  - Master-master
- **Availability targets**: 99.9% (3 nines), 99.99% (4 nines)

## Node.js Developer Notes

- Your Node.js app running on a single VPS = **vertical scaling**
- Adding more VPS instances behind a load balancer = **horizontal scaling**
- Redis as a cache = **application caching**
- PM2 cluster mode = basic **load balancing**

## Sources
- [A word on scalability](http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html)
- [Scalability, availability, stability, patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns/)
- [Harvard Scalability Lecture](https://www.youtube.com/watch?v=-W9F__D3oY4)
