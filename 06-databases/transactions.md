# Database Transactions

## Rabbit hole

- [What happens if two users try to modify the same database record at exactly the same time?](../10-rabbit-holes/what-if-two-users-update-the-same-record.md)

**Answer:** A transaction groups database operations so they succeed or fail as a unit and obey isolation rules. The database may serialize conflicting writes, lock records, or detect a conflict and abort one transaction; application logic can then retry or ask the user to resolve it.
