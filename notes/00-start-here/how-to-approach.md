# How to Approach a System Design Interview

## The Interview is a Conversation

System design interviews are **open-ended**. You are expected to **lead** the discussion.

## Step 1: Outline Use Cases, Constraints, and Assumptions

Gather requirements and scope the problem. Ask questions to clarify use cases and constraints. Discuss assumptions.

**Questions to ask:**
- Who is going to use it?
- How are they going to use it?
- How many users are there?
- What does the system do?
- What are the inputs and outputs?
- How much data do we expect to handle?
- How many requests per second?
- What is the read-to-write ratio?

**As a Node.js developer, think about:**
- What endpoints would I need?
- What would my API contracts look like?
- What database would I pick?

## Step 2: Create a High-Level Design

Outline a high-level design with all important components.
- Sketch the main components and connections
- Justify your ideas

**Components typically include:**
- Clients (web, mobile)
- Load balancer
- Application servers
- Database
- Cache
- CDN
- Message queue

## Step 3: Design Core Components

Dive into details for each core component.

For example, designing a URL shortener:
- Generating and storing a hash (MD5, Base62)
- Hash collisions handling
- SQL or NoSQL?
- Database schema
- Translating hash to full URL (database lookup)
- API and OOP design

## Step 4: Scale the Design

Identify and address bottlenecks given constraints.

**Common scaling additions:**
- Load balancer
- Horizontal scaling
- Caching
- Database sharding
- Async processing

**Ask yourself:**
- What is the bottleneck right now?
- What happens at 10x traffic?
- What happens at 100x traffic?

## Back-of-the-Envelope Calculations

You might be asked to estimate by hand. Key resources:
- [Powers of two table](#)
- [Latency numbers every programmer should know](#)
- Use the approach: "How many requests/sec? How much storage? How much bandwidth?"

**Example calculation for a URL shortener:**
- 100M URLs, 10K reads/sec, 1K writes/sec
- Storage: 100M × ~100 bytes = ~10 GB
- Bandwidth: 10K × ~1KB = ~10 MB/sec read

## Source(s) and Further Reading
- [How to ace a systems design interview](https://web.archive.org/web/20210505130322/https://www.palantir.com/2011/10/how-to-rock-a-systems-design-interview/)
- [The system design interview](http://www.hiredintech.com/system-design)
- [System design template](https://leetcode.com/discuss/career/229177/My-System-Design-Template)

## Node.js Developer Tips

- Start with what you know: Express/Fastify APIs
- Think about your deployment: VPS → Load balancer → Multiple instances
- Your instinct is usually correct for the basics
- The interview is about trade-offs, not perfect answers
