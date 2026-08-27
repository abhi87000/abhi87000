# Abhishek Gautam

Backend engineer, ~3 years, New Delhi (IST). Java and Spring Boot, mostly in fintech.

I work on the part of a system where correctness *is* the product — money movement,
settlement, reconciliation, and keeping all of it right when the same event arrives twice.

**Now** — SDE-2 at Techmojo, owning the promotion engines on a B2B platform processing
900M+ events a month.

**Before** — SDE-1 at SOLV (Standard Chartered), helping build the reconciliation and
settlement backend from scratch for an escrow-backed B2B marketplace: 50+ REST endpoints,
100K+ orders a day, 99.9% uptime.

### Problems I've actually had to solve

**Exactly-once payouts over at-least-once delivery.** Kafka redelivers, so exactly-once has
to be built rather than assumed. A unique settlement ID plus a status state machine meant a
redelivered event could never pay a seller twice — with no lock anywhere in the path.

**Reconciliation against an external partner.** Daily payment-partner statements matched
against our own records, normalised for commission, tax and banking-holiday shifts before
anything reached the payout file.

**An 11-day silent outage nobody could reproduce.** A Quartz trigger stuck in BLOCKED,
traced to an HTTP call with no read timeout parking a thread in socket read forever. Cluster
recovery only handles dead instances, so it never self-healed. The absence of a timeout is
the absence of a failure signal.

**Scaling in the right order.** Query and index tuning, Redis caching, multithreading and JVM
tuning first (~15% latency cut), then horizontal scaling, with ShedLock keeping schedulers
single-execution across instances.

### Stack

`Java 17/21` `Spring Boot` `Spring Data JPA / Hibernate` `REST`
`Apache Kafka` `Redis` `distributed locks` `idempotency`
`MySQL` `PostgreSQL` `MongoDB` `stored procedures` `query optimisation`
`Docker` `Kubernetes` `Jenkins` `AWS (EC2, S3, RDS)` `Git` `Linux`

Claude Code, Codex and MCP servers are part of my daily workflow.

### Also

1250+ DSA and SQL problems solved, 500+ on LeetCode.

### Reach me

[LinkedIn](https://www.linkedin.com/in/abhishek8700) · gautamabhishek87000@gmail.com

Open to fully remote backend roles.
