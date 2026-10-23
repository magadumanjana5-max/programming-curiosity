# Rabbit Hole 7: What If Two Users Update the Same Record?

**Question:** What happens if two users try to modify the same database record at exactly the same time?

**Answer:** The database applies its concurrency rules: it may lock the record, order the writes, detect a conflict, or let a later update overwrite an earlier one. Transactions and isolation levels determine which outcomes are allowed. Applications can use optimistic version checks and ask a user to retry or merge changes rather than silently losing an update.

- **WHY:** Concurrent updates must preserve data consistency and avoid surprising lost changes.
- **WHAT:** A conflict occurs when operations overlap on the same data.
- **HOW:** Locks, isolation, version numbers, and conflict-detection logic coordinate writes.
- **WHERE:** Coordination is usually enforced by the database, with application logic handling conflict outcomes.
- **WHEN:** It matters when users or background jobs can edit shared records concurrently.
- **WHO:** The database engine and application jointly determine the behavior users see.
- **WHAT IF:** A transaction is aborted or times out? The application should handle the error and retry only when that is safe.

Explore [database transactions](../06-databases/transactions.md).
