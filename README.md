# 📐 System Design Notes

<div align="center">

[![Status](https://img.shields.io/badge/phase-00--start--here-blue)]()
[![Progress](https://img.shields.io/badge/progress-0%25-lightgrey)]()
[![Node.js](https://img.shields.io/badge/background-Node.js%20Backend-green)]()
[![Target](https://img.shields.io/badge/target-System%20Design%20Interview-orange)]()

</div>

> Study notes based on [donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer) — a comprehensive open-source guide for designing large-scale systems and preparing for system design interviews.

---

## 🚀 About

| | |
|---|---|
| **Role** | Junior Backend Developer |
| **Stack** | Node.js, Express/Fastify, MongoDB, PostgreSQL, Redis |
| **Experience** | Building APIs, deploying full-stack projects on VPS |
| **Goal** | Master system design principles and ace technical interviews |
| **Timeline** | 8–12 weeks |
| **Primary Resource** | [system-design-primer](https://github.com/donnemartin/system-design-primer) |

---

## 📂 Directory Structure

```
notes/
├── 00-start-here/          # Scalability intro & interview approach
├── 01-fundamentals/        # CAP theorem, consistency, performance
├── 02-core-concepts/       # DNS, CDN, Load balancer, Reverse proxy
├── 03-infrastructure/      # Microservices, Service discovery
├── 04-application/         # Application caching strategies
├── 05-database/            # RDBMS, NoSQL, Sharding, Replication
├── 06-cache/               # Cache patterns & invalidation
├── 07-asynchronism/        # Message queues, Task queues, Back pressure
├── 08-communication/       # TCP, UDP, RPC, REST
├── 09-security/            # Security principles
├── 10-solutions/           # Practice problems (Pastebin, Twitter, etc.)
├── 11-ood/                 # Object-oriented design (LRU, Call center, etc.)
├── 12-appendices/          # Latency numbers, Powers of two, Real-world arches
├── nodejs-bridge.md        # Node.js → System Design mapping guide
├── PROGRESS.md             # Detailed progress tracker & weekly log
├── template.md             # Note-taking template
└── README.md               # This file
```

---

## 📋 Study Roadmap

### Phase 1: Foundations
> *Scalability concepts, trade-offs, and CAP theorem*

| Topic | File | Status |
|---|---|---|
| Scalability Video Lecture | `00-start-here/scalability.md` | ⬜ |
| How to Approach a System Design Question | `00-start-here/how-to-approach.md` | ⬜ |
| Performance vs Scalability | `01-fundamentals/performance-vs-scalability.md` | ⬜ |
| Latency vs Throughput | `01-fundamentals/latency-vs-throughput.md` | ⬜ |
| CAP Theorem (CP vs AP) | `01-fundamentals/cap-theorem.md` | ⬜ |
| Consistency Patterns | `01-fundamentals/consistency-patterns.md` | ⬜ |

### Phase 2: Infrastructure
> *DNS, CDNs, Load Balancers, Reverse Proxies*

| Topic | File | Status |
|---|---|---|
| Domain Name System (DNS) | `02-core-concepts/dns.md` | ⬜ |
| Content Delivery Network (CDN) | `02-core-concepts/cdn.md` | ⬜ |
| Load Balancer (L4 & L7) | `02-core-concepts/load-balancer.md` | ⬜ |
| Reverse Proxy | `02-core-concepts/reverse-proxy.md` | ⬜ |
| Horizontal Scaling | `02-core-concepts/load-balancer.md` | ⬜ |

### Phase 3: Application Layer & Microservices
> *Application architecture and service discovery*

| Topic | File | Status |
|---|---|---|
| Application Layer | `03-infrastructure/microservices.md` | ⬜ |
| Microservices | `03-infrastructure/microservices.md` | ⬜ |
| Service Discovery | `03-infrastructure/service-discovery.md` | ⬜ |

### Phase 4: Data Layer
> *Databases, caching, and data management*

| Topic | File | Status |
|---|---|---|
| RDBMS & Scaling | `05-database/rdbms.md` | ⬜ |
| NoSQL Databases | `05-database/nosql.md` | ⬜ |
| SQL vs NoSQL | `05-database/sql-vs-nosql.md` | ⬜ |
| Caching Strategies | `06-cache/cache-strategies.md` | ⬜ |
| Cache-Aside / Write-Through / Write-Behind | `06-cache/cache-strategies.md` | ⬜ |

### Phase 5: Advanced Concepts
> *Asynchronism, communication protocols, and security*

| Topic | File | Status |
|---|---|---|
| Message Queues & Task Queues | `07-asynchronism/message-queues.md` | ⬜ |
| Back Pressure | `07-asynchronism/message-queues.md` | ⬜ |
| TCP vs UDP | `08-communication/tcp-vs-udp.md` | ⬜ |
| RPC vs REST | `08-communication/rpc-vs-rest.md` | ⬜ |
| Security | `09-security/security.md` | ⬜ |

### Phase 6: Practice Problems
> *Real-world system design with solutions*

| Problem | Solution Link | File | Status |
|---|---|---|---|
| Pastebin / Bit.ly | [Solution](../../system-design-primer/solutions/system_design/pastebin/) | `10-solutions/pastebin.md` | ⬜ |
| Twitter Timeline & Search | [Solution](../../system-design-primer/solutions/system_design/twitter/) | `10-solutions/twitter.md` | ⬜ |
| Web Crawler | [Solution](../../system-design-primer/solutions/system_design/web_crawler/) | `10-solutions/web-crawler.md` | ⬜ |
| Mint.com | [Solution](../../system-design-primer/solutions/system_design/mint/) | `10-solutions/mint.md` | ⬜ |
| Social Graph | [Solution](../../system-design-primer/solutions/system_design/social_graph/) | `10-solutions/social-graph.md` | ⬜ |
| Query Cache | [Solution](../../system-design-primer/solutions/system_design/query_cache/) | `10-solutions/query-cache.md` | ⬜ |
| Sales Ranking | [Solution](../../system-design-primer/solutions/system_design/sales_rank/) | `10-solutions/sales-rank.md` | ⬜ |
| AWS Scaling | [Solution](../../system-design-primer/solutions/system_design/scaling_aws/) | `10-solutions/scaling-aws.md` | ⬜ |

### Phase 7: Object-Oriented Design
> *OOP interview questions with solutions*

| Problem | File | Status |
|---|---|---|
| Hash Map | `11-ood/hash-map.md` | ⬜ |
| LRU Cache | `11-ood/lru-cache.md` | ⬜ |
| Call Center | `11-ood/call-center.md` | ⬜ |
| Parking Lot | `11-ood/parking-lot.md` | ⬜ |

### Phase 8: Appendices & Review
> *Quick reference and real-world architectures*

| Topic | File | Status |
|---|---|---|
| Powers of Two | `12-appendices/powers-of-two.md` | ⬜ |
| Latency Numbers | `12-appendices/latency-numbers.md` | ⬜ |
| Real-World Architectures | `12-appendices/real-world-architectures.md` | ⬜ |

---

## 🧭 How to Study

```
1. Read       → system-design-primer/README.md (corresponding section)
2. Watch      → Linked videos and resources
3. Write      → Your notes in the appropriate folder
4. Diagram    → Sketch the architecture
5. Calculate  → Back-of-envelope estimates
6. Practice   → Solve the related interview question
7. Review     → Anki flashcards (system-design-primer/resources/flash_cards/)
```

---

## 📊 Progress

```
Phase 1: [████░░░░░░] 10%
Phase 2: [░░░░░░░░░░]  0%
Phase 3: [░░░░░░░░░░]  0%
Phase 4: [░░░░░░░░░░]  0%
Phase 5: [░░░░░░░░░░]  0%
Phase 6: [░░░░░░░░░░]  0%
Phase 7: [░░░░░░░░░░]  0%
Phase 8: [░░░░░░░░░░]  0%

Overall: [█░░░░░░░░░] 5%
```

Detailed progress: [PROGRESS.md](./PROGRESS.md)

---

## 🔗 Quick Links

| Resource | Link |
|---|---|
| 📖 Main Guide | [system-design-primer/README.md](../../system-design-primer/README.md) |
| 📝 Study Guide | [study_guide.png](../../system-design-primer/resources/study_guide.png) |
| 🃏 Anki Flashcards | [flash_cards/](../../system-design-primer/resources/flash_cards/) |
| 💡 Solutions | [solutions/](../../system-design-primer/solutions/) |
| 📘 Node.js Bridge | [nodejs-bridge.md](./nodejs-bridge.md) |
| 📈 Progress | [PROGRESS.md](./PROGRESS.md) |
| 📝 Note Template | [template.md](./template.md) |

---

## 💡 Key Principles

> **Everything is a trade-off.**
> There is no perfect architecture — only the right trade-offs for your constraints.

- **Performance** vs **Scalability**
- **Latency** vs **Throughput**
- **Consistency** vs **Availability**
- **Simplicity** vs **Flexibility**
- **Cost** vs **Performance**

---

## 📚 Contributing

This is a personal study workspace. Notes are being built as I work through the [system-design-primer](https://github.com/donnemartin/system-design-primer) curriculum.

---

## 📄 License

Study notes based on [donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer), which is licensed under [MIT](LICENSE.txt).
