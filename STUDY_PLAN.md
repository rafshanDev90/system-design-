# System Design Study Plan

> **Background**: Junior backend developer with Node.js experience. Building APIs and deploying full-stack projects on VPS. Moving to system design.
>
> **Primary Resource**: [system-design-primer](https://github.com/donnemartin/system-design-primer) by donnemartin

---

## Timeline Estimate: 8–12 Weeks

Adjust based on your schedule. The study guide in the primer suggests:

| Timeline | Focus |
|---|---|
| **Short** | Breadth + some interview questions |
| **Medium** | Breadth + some depth + many questions |
| **Long** | Breadth + more depth + most questions |

---

## Phase 1: Foundations (Week 1–2)

### Topics
- [ ] Step 1: Review scalability video lecture (Harvard)
- [ ] Step 2: Review scalability article (lecloud.net)
- [ ] Performance vs scalability
- [ ] Latency vs throughput
- [ ] Availability vs consistency
- [ ] CAP theorem (CP vs AP)
- [ ] Consistency patterns (weak, eventual, strong)
- [ ] Availability patterns (fail-over, replication)

### Key Takeaways
- Understand the difference between performance and scalability
- Know the CAP theorem and its trade-offs
- Understand consistency models

### Files
- `notes/00-start-here/`
- `notes/01-fundamentals/`

---

## Phase 2: Infrastructure Layer (Week 3–4)

### Topics
- [ ] Domain Name System (DNS)
- [ ] Content Delivery Network (CDN) — push vs pull
- [ ] Load Balancer — active-passive, active-active, L4 vs L7
- [ ] Horizontal scaling
- [ ] Reverse proxy (web server)
- [ ] Load balancer vs reverse proxy
- [ ] Application layer — microservices
- [ ] Service discovery

### Key Takeaways
- Understand how requests flow from client to server
- Know when to use load balancers, CDNs, reverse proxies
- Understand horizontal vs vertical scaling
- Know the difference between load balancer and reverse proxy

### Files
- `notes/02-core-concepts/`
- `notes/03-infrastructure/`

---

## Phase 3: Data Layer (Week 5–6)

### Topics
- [ ] RDBMS — master-slave, master-master, federation, sharding, denormalization, SQL tuning
- [ ] NoSQL — key-value, document, wide column, graph
- [ ] SQL or NoSQL decision framework
- [ ] Cache — client, CDN, web server, database, application caching
- [ ] Cache strategies — cache-aside, write-through, write-behind, refresh-ahead

### Key Takeaways
- Know when to use SQL vs NoSQL
- Understand database scaling techniques (replication, sharding, federation)
- Master cache patterns and strategies
- Understand cache invalidation

### Files
- `notes/04-application/`
- `notes/05-database/`
- `notes/06-cache/`

---

## Phase 4: Advanced Concepts (Week 7–8)

### Topics
- [ ] Asynchronism — message queues, task queues, back pressure
- [ ] Communication — TCP vs UDP, RPC, REST
- [ ] Security

### Key Takeaways
- Understand message queues and when to use async processing
- Know the difference between TCP/UDP, RPC, and REST
- Understand basic security principles

### Files
- `notes/07-asynchronism/`
- `notes/08-communication/`
- `notes/09-security/`

---

## Phase 5: Practice Problems (Week 9–11)

### System Design Questions (solutions provided)
1. [ ] **Pastebin / Bit.ly** — URL shortening service
2. [ ] **Twitter timeline & search** — Feed and search system
3. [ ] **Web crawler** — Internet crawling system
4. [ ] **Mint.com** — Financial tracking dashboard
5. [ ] **Social network data structures** — Graph data model
6. [ ] **Key-value store for search engine** — Query cache
7. [ ] **Amazon sales ranking** — Category feature
8. [ ] **Scaling to millions on AWS** — Cloud architecture

### Object-Oriented Design Questions
1. [ ] Hash map
2. [ ] LRU cache
3. [ ] Call center
4. [ ] Deck of cards
5. [ ] Parking lot
6. [ ] Chat server

### Files
- `notes/10-solutions/`
- `notes/11-ood/`

---

## Phase 6: Appendices & Review (Week 12)

### Topics
- [ ] Powers of two table
- [ ] Latency numbers every programmer should know
- [ ] Real-world architectures
- [ ] Company architectures (Netflix, Google, etc.)
- [ ] Company engineering blogs
- [ ] Additional system design interview questions

### Files
- `notes/12-appendices/`

---

## Study Methodology

### For Each Topic:
1. **Read** the corresponding section in `system-design-primer/README.md`
2. **Watch** any linked videos
3. **Write** your own notes in `notes/` directory
4. **Draw** the architecture diagram
5. **Practice** the back-of-envelope calculations
6. **Solve** the related interview question

### For Each Solution:
1. **Attempt** the exercise without looking at the solution
2. **Compare** your design with the provided solution
3. **Note** the trade-offs and why certain choices were made
4. **Modify** the design with different constraints

### Weekly Review:
- Review Anki flashcards (in `system-design-primer/resources/flash_cards/`)
- Revisit weak areas
- Do back-of-envelope calculations practice

---

## Resources in This Repo

| Resource | Path |
|---|---|
| Main guide | `system-design-primer/README.md` |
| Study guide diagram | `system-design-primer/resources/study_guide.png` |
| Anki flashcards | `system-design-primer/resources/flash_cards/` |
| Solution templates | `system-design-primer/solutions/system_design/template/` |
| Practice solutions | `system-design-primer/solutions/system_design/` |
| OOD solutions | `system-design-primer/solutions/object_oriented_design/` |

---

## Progress Tracker

| Phase | Topics | Status |
|---|---|---|
| Phase 1: Foundations | ⬜⬜⬜⬜⬜⬜⬜ | Not started |
| Phase 2: Infrastructure | ⬜⬜⬜⬜⬜⬜⬜⬜⬜ | Not started |
| Phase 3: Data Layer | ⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ | Not started |
| Phase 4: Advanced | ⬜⬜⬜⬜⬜⬜⬜ | Not started |
| Phase 5: Practice | ⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜⬜ | Not started |
| Phase 6: Review | ⬜⬜⬜⬜⬜ | Not started |

---

*Last updated: 2026-09-23*
