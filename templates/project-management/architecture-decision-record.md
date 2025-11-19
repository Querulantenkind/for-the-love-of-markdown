<!-- 
  TEMPLATE: Architecture Decision Record (ADR)
  COMPLEXITY: Medium
  FEATURES: Structured academic layout, Status badges, Decision log
  USE CASE: Documenting significant architectural decisions in a project.
-->

# ADR-001: [Title of the Decision]

| Status | Date | Author | Deciders |
| :--- | :--- | :--- | :--- |
| ![Status](https://img.shields.io/badge/Status-Proposed-yellow) | 2025-11-19 | @username | @team-lead, @architect |

---

## 1. Context and Problem Statement

[Describe the context and problem statement, e.g., "We need to choose a database for the new user analytics service. The current solution (PostgreSQL) is struggling with write throughput."]

**Constraints:**
- Must handle 10k writes/sec.
- Must support time-series queries.
- Budget: < $500/month.

## 2. Decision Drivers

- 🚀 **Performance**: Write speed is critical.
- 💰 **Cost**: Must fit within startup budget.
- 🧠 **Maintainability**: Team is familiar with SQL but willing to learn NoSQL.
- 🔒 **Compliance**: Data must be encrypted at rest.

## 3. Considered Options

### Option A: PostgreSQL (Optimized)
- **Pros**: Team knows it well; ACID compliance.
- **Cons**: Vertical scaling is expensive; partitioning is complex.

### Option B: MongoDB
- **Pros**: Flexible schema; good write performance.
- **Cons**: Weak joins; eventual consistency model.

### Option C: TimescaleDB
- **Pros**: SQL interface; optimized for time-series; built on Postgres.
- **Cons**: Niche knowledge required for tuning.

## 4. Decision Outcome

Chosen option: **Option C: TimescaleDB**

**Reasoning:**
TimescaleDB offers the best balance of performance and familiarity. Since it is an extension of PostgreSQL, we can leverage existing drivers and tooling while gaining the write throughput benefits of a time-series database.

### Positive Consequences
- Write throughput increased by 5x in benchmarks.
- No need to rewrite ORM layer completely.

### Negative Consequences
- New operational overhead for managing Timescale specific features (chunks, compression).

## 5. Validation

We will validate this decision by:
1. Running a load test simulating 2x peak traffic.
2. Measuring query latency for the top 5 dashboard queries.

---

## 🔗 Links

- [RFC-123: Database Evaluation](../rfcs/rfc-123.md)
- [Benchmark Results](../benchmarks/db-results.md)
