# Node.js to System Design: A Bridge Guide

## Your Current Skills → System Design Concepts

| What You Know | What It Maps To |
|---|---|
| Express/Fastify server | Application layer, reverse proxy |
| REST APIs | Communication patterns (REST vs RPC) |
| MongoDB/PostgreSQL | Database layer (NoSQL vs SQL) |
| Redis | Caching strategies |
| PM2 cluster mode | Load balancing, horizontal scaling |
| VPS deployment | Single server = vertical scaling |
| Docker containers | Microservices, service discovery |
| Nginx | Reverse proxy, load balancer |
| Event loop / async/await | Asynchronism, message queues |
| JWT auth | Security |
| Nginx reverse proxy config | Load balancer vs reverse proxy |
| Deploying on VPS | Infrastructure fundamentals |
| npm/yarn | Dependency management at scale |

## Common Scaling Problems You'll Face

### 1. Single VPS Bottleneck
**You**: One Express server on one VPS
**Problem**: Can't handle more than X concurrent connections
**Solution**: Load balancer + multiple instances

### 2. Database Overload
**You**: MongoDB/PostgreSQL on same VPS
**Problem**: Queries slow down under load
**Solution**: Read replicas, caching, connection pooling

### 3. Memory Leaks Under Load
**You**: Node.js app with growing memory usage
**Problem**: OOM kills, garbage collection pauses
**Solution**: Horizontal scaling, monitoring, proper memory management

### 4. File Uploads Blocking Event Loop
**You**: Sync file operations in Express
**Problem**: Event loop blocked, poor throughput
**Solution**: Async processing, message queues, CDN for static files

### 5. No Cache Layer
**You**: Every request hits the database
**Problem**: Repeated queries for same data
**Solution**: Redis cache, cache-aside pattern

## Key Design Patterns for Node.js Developers

### Caching with Redis
```
Client → Load Balancer → App Server (Node.js) → Redis Cache
                                                  ↓ (cache miss)
                                              PostgreSQL
```

### Horizontal Scaling
```
Client → Load Balancer → App Server 1 (Node.js)
                   → App Server 2 (Node.js)
                   → App Server 3 (Node.js)
                         ↓
                    PostgreSQL (with replicas)
                    Redis (cache)
```

### Async Processing
```
Client → Express → Message Queue → Worker (Node.js)
         (HTTP response 202)
```

## Study Order Recommendation

Given your Node.js background, I recommend:

1. **Start with what you know**: Reverse proxy, load balancing, caching
2. **Connect to your experience**: How does your VPS deployment relate to scaling?
3. **Move to databases**: SQL vs NoSQL - you already use both
4. **Tackle async**: Message queues are natural extensions of Node.js async
5. **Practice with problems**: Start with Pastebin/Bit.ly (familiar concept)

## Tools to Explore Next
- **Docker Compose**: Multi-service deployments
- **Nginx**: Reverse proxy configuration
- **Redis**: Caching patterns
- **Kafka/RabbitMQ**: Message queues
- **PostgreSQL read replicas**: Database scaling
- **AWS/GCP**: Cloud architecture (scaling_aws solution)
