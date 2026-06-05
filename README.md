# SDE_Roadmap
# 🎯 Junior SDE Learning Plan — 

> **Goal:** Land a Junior Java SDE role 

> **Estimated prep time:** 4–5 months focused study

---

## 🔴 Tier 1 — Interview Dealbreakers (Start Immediately)

> These will get you screened out if missing. Learn these before anything else.

---

### 1. Multi-threading & Concurrency
**Timeline:** 3–4 weeks
**Why:** Asked in every Java interview at this level. Non-negotiable.

**Topics to cover:**
- [ ] Thread lifecycle (`new`, `runnable`, `blocked`, `waiting`, `terminated`)
- [ ] `synchronized` keyword — method vs block level
- [ ] `volatile` keyword — visibility guarantees
- [ ] `ReentrantLock` and `Condition`
- [ ] `wait()`, `notify()`, `notifyAll()`
- [ ] `ExecutorService`, `ThreadPoolExecutor`, `Callable`, `Future`
- [ ] `CompletableFuture` — chaining async tasks
- [ ] `BlockingQueue` — producer-consumer pattern
- [ ] Deadlock — how to detect and prevent
- [ ] `ConcurrentHashMap` vs `Collections.synchronizedMap()`
- [ ] Java Memory Model basics (happens-before)

**Practice problems:**
- [ ] Build a producer-consumer from scratch using `BlockingQueue`
- [ ] Implement a thread-safe singleton (double-checked locking)
- [ ] Build a simple rate limiter using `ReentrantLock`
- [ ] Print odd/even numbers using two threads alternately

**Resources:** Java Concurrency in Practice (book) · Baeldung concurrency tutorials

---

### 2. Java Collections Deep Dive
**Timeline:** 1–2 weeks
**Why:** Mandatory for interviews AND daily coding. Interviewers ask internals, not just usage.

**Topics to cover:**
- [ ] `ArrayList` vs `LinkedList` — when to use which
- [ ] `HashMap` internals — hashing, buckets, load factor, rehashing
- [ ] `LinkedHashMap` — insertion order vs access order
- [ ] `TreeMap` — Red-Black tree, sorted keys, `NavigableMap`
- [ ] `HashSet` vs `TreeSet` vs `LinkedHashSet`
- [ ] `PriorityQueue` — min/max heap, custom `Comparator`
- [ ] `ArrayDeque` as stack and queue
- [ ] `ConcurrentHashMap` — segment locking vs `CAS`
- [ ] `CopyOnWriteArrayList` — when and why
- [ ] Fail-fast vs fail-safe iterators
- [ ] `Comparable` vs `Comparator` — sorting custom objects

**Practice problems:**
- [ ] Implement `LRU Cache` using `LinkedHashMap`
- [ ] Top K frequent elements using `PriorityQueue`
- [ ] Group anagrams using `HashMap`

---

### 3. DSA in Java (LeetCode)
**Timeline:** 4–6 weeks (ongoing, daily practice)
**Why:** Screened in every SDE round. Solve in Java — not Python.

**Topics to cover:**
- [ ] Arrays & strings — two pointers, sliding window
- [ ] HashMap & HashSet patterns
- [ ] Stack and Queue problems
- [ ] Linked lists — reversal, cycle detection, merge
- [ ] Binary search — standard + rotated array variants
- [ ] Trees — BFS, DFS, level order, LCA
- [ ] Graphs — BFS, DFS, topological sort, union-find
- [ ] Dynamic programming — 1D, 2D, memoization
- [ ] Recursion and backtracking

**Java-specific must-knows:**
- [ ] `PriorityQueue` with lambda comparator: `new PriorityQueue<>((a,b) -> a-b)`
- [ ] `Map.getOrDefault()`, `Map.computeIfAbsent()`
- [ ] `Collections.sort()` with `Comparator.comparing()`
- [ ] `Arrays.sort()` vs `Arrays.stream().sorted()`
- [ ] `StringBuilder` for string manipulation

**Target:** 80 problems on LeetCode (60% easy, 40% medium) in Java

---

### 4. Low-Level Design (LLD)
**Timeline:** 2–3 weeks
**Why:** Junior SDE rounds include "design this class" problems. Very common.

**Topics to cover:**
- [ ] SOLID principles — with Java examples for each
- [ ] Design Patterns:
  - [ ] Singleton (thread-safe)
  - [ ] Factory & Abstract Factory
  - [ ] Builder
  - [ ] Strategy
  - [ ] Observer
  - [ ] Decorator
- [ ] UML class diagrams — reading and drawing
- [ ] API design — request/response models, error handling

**Classic LLD problems to practice:**
- [ ] Design a Parking Lot
- [ ] Design an LRU Cache
- [ ] Design a Library Management System
- [ ] Design a Vending Machine
- [ ] Design Snake and Ladder game

---

## 🔵 Tier 2 — AWS Cloud Skills (Critical Gap)

> Zero AWS on your resume is a major blocker for this specific JD. Use AWS Free Tier.

---

### 5. AWS Lambda & ECS
**Timeline:** 1–2 weeks

- [ ] What is serverless? Lambda execution model
- [ ] Lambda triggers — API Gateway, SQS, S3 events
- [ ] Lambda limits — timeout, memory, payload size
- [ ] ECS basics — clusters, tasks, services, task definitions
- [ ] Fargate vs EC2 launch types
- [ ] **Project:** Deploy your Finance Tracker as a Lambda function

---

### 6. DynamoDB
**Timeline:** 1 week

- [ ] NoSQL vs SQL — when to choose DynamoDB
- [ ] Partition key and sort key design
- [ ] GSI (Global Secondary Index) and LSI
- [ ] Read/write capacity modes — on-demand vs provisioned
- [ ] Single-table design pattern
- [ ] DynamoDB Streams
- [ ] **Project:** Replace MySQL in Finance Tracker with DynamoDB for one entity

---

### 7. SNS & SQS — Messaging
**Timeline:** 1 week

- [ ] SQS — standard vs FIFO queues
- [ ] Message visibility timeout, dead-letter queues (DLQ)
- [ ] SNS — topics, subscriptions, fan-out pattern
- [ ] SNS → SQS fan-out architecture
- [ ] At-least-once vs exactly-once delivery
- [ ] **Project:** Add an SNS notification when a new expense is added in Finance Tracker

---

### 8. AWS Fundamentals
**Timeline:** 1 week

- [ ] IAM — roles, policies, least privilege principle
- [ ] VPC basics — subnets, security groups, NACLs
- [ ] CloudWatch — logs, metrics, alarms
- [ ] S3 — buckets, storage classes, presigned URLs
- [ ] API Gateway — REST APIs, integrations with Lambda

---

## 🟡 Tier 3 — Backend Depth (Important)

---

### 9. Distributed Systems Concepts
**Timeline:** 2 weeks

- [ ] CAP theorem — consistency vs availability vs partition tolerance
- [ ] Eventual consistency
- [ ] Idempotency — why it matters in APIs
- [ ] Rate limiting strategies — token bucket, leaky bucket
- [ ] Circuit breaker pattern (Resilience4j in Spring Boot)
- [ ] Retry with exponential backoff
- [ ] Load balancing basics

---

### 10. Unit & Integration Testing
**Timeline:** 1 week

- [ ] JUnit 5 — `@Test`, `@BeforeEach`, `@AfterEach`, `@ParameterizedTest`
- [ ] Mockito — `@Mock`, `@InjectMocks`, `when().thenReturn()`, `verify()`
- [ ] Testing Spring Boot controllers with `@WebMvcTest`
- [ ] Testing services with `@SpringBootTest`
- [ ] TestContainers — spinning up real DB for integration tests
- [ ] Code coverage basics with JaCoCo
- [ ] **Action:** Add JUnit tests to your Finance Tracker project (aim for 60% coverage)

---

### 11. API Design & Error Handling
**Timeline:** 1 week

- [ ] REST best practices — naming, status codes, versioning (`/v1/`)
- [ ] Global exception handler in Spring Boot (`@ControllerAdvice`)
- [ ] Custom error response structure
- [ ] Input validation with `@Valid`, `@NotNull`, `@Size`
- [ ] Idempotency keys for POST requests
- [ ] Pagination — `Pageable` in Spring Data JPA
- [ ] API documentation with Swagger / OpenAPI 3

---

### 12. Production Debugging
**Timeline:** 1 week

- [ ] Reading structured logs — log levels, correlation IDs
- [ ] CloudWatch Logs Insights queries
- [ ] Thread dump analysis — identifying deadlocks
- [ ] Heap dump basics — OutOfMemoryError diagnosis
- [ ] Distributed tracing concepts (AWS X-Ray / Jaeger)
- [ ] Key metrics to watch: latency, error rate, throughput, saturation

---

## 🟢 Tier 4 — Good to Have

---

### 13. Docker & Containerisation
**Timeline:** 1 week

- [ ] Writing a `Dockerfile` for a Spring Boot app
- [ ] Docker images, containers, volumes
- [ ] `docker-compose` for local dev (app + MySQL + Redis)
- [ ] Container networking basics
- [ ] Connects directly to ECS knowledge

---

### 14. Leverage Your Performance Testing Background
**Timeline:** Ongoing

- [ ] Reframe LoadRunner experience as "load and scalability analysis" on resume
- [ ] Learn JMeter or k6 — run load tests against your own Spring Boot app
- [ ] Document findings: p99 latency, throughput under load, bottlenecks found
- [ ] This is a genuine differentiator — most junior Java devs have never done this

---

### 15. Technical Documentation
**Timeline:** Ongoing

- [ ] Write a README for each of your GitHub projects (setup, architecture, API docs)
- [ ] Learn Swagger annotations — auto-generate API docs from code
- [ ] Write one Architecture Decision Record (ADR) for a choice you made in Finance Tracker
- [ ] Practice explaining technical decisions in plain English

---

### 16. Kafka Basics
**Timeline:** 1 week (after SNS/SQS)

- [ ] Topics, partitions, offsets
- [ ] Producers and consumers
- [ ] Consumer groups and rebalancing
- [ ] Kafka vs SQS — when to use which
- [ ] Spring Kafka — `@KafkaListener`

---

## 📅 Suggested Monthly Plan

| Month | Focus |
|-------|-------|
| Month 1 | Multi-threading + Java Collections + start LeetCode daily |
| Month 2 | LLD + DSA (trees, graphs, DP) + add tests to Finance Tracker |
| Month 3 | AWS (Lambda, DynamoDB, SNS/SQS) + deploy Finance Tracker to AWS |
| Month 4 | Distributed systems + API design + production debugging |
| Month 5 | Mock interviews + resume update + apply aggressively |

---

## 🏗️ Project Action Items

These will directly improve your resume bullet points:

- [ ] Add multi-threading to Finance Tracker (async expense processing with `CompletableFuture`)
- [ ] Add JUnit + Mockito tests (target 60% coverage, mention in resume)
- [ ] Deploy Finance Tracker to AWS Lambda + DynamoDB
- [ ] Add SNS notification on expense creation
- [ ] Write Swagger docs and link in GitHub README
- [ ] Run a JMeter load test on your own API — document results

---

## 📌 Resume Keywords to Add (Once Learned)

Add these exact terms to your resume skills or project descriptions:

`multi-threading` · `concurrency` · `Java Collections` · `ExecutorService` · `CompletableFuture` · `JUnit 5` · `Mockito` · `AWS Lambda` · `DynamoDB` · `SNS` · `SQS` · `distributed systems` · `low-level design` · `SOLID principles` · `design patterns` · `idempotency` · `rate limiting` · `CloudWatch` · `Docker`

---
