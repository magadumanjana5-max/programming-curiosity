# Database Indexes

## Curiosity questions

69. Why do we need indexes?
   **Answer:** An index lets a database find matching rows without scanning every row, much like a book index. It can speed reads but consumes storage and adds work to inserts, updates, and deletes, so indexes should match real query patterns.
