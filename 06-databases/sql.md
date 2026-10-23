# SQL Databases

## Curiosity questions

61. Why can’t we simply store everything in Python variables?
   **Answer:** Variables live in a process and usually disappear when it exits; they are also not automatically shared reliably among servers or users. Databases persist data, support queries and concurrent access, and provide controls such as transactions and permissions.
62. Why do applications need databases?
   **Answer:** Databases organize persistent data and let applications retrieve and update it consistently. They provide indexing, concurrency control, access management, and recovery features that would be difficult to build safely from ordinary variables and files alone.
63. What happens when you click “Save”?
   **Answer:** Usually the application validates the input, sends it to a backend, and the backend checks permissions and writes through a database driver. The database processes the operation and may commit it to durable storage; the result is sent back to the user interface.
64. Where does the data physically go?
   **Answer:** A database stores data on persistent media such as SSDs, often with memory buffers, logs, and replicas. The exact machines and locations depend on deployment; cloud databases still run on physical infrastructure managed by a provider.
65. What is a table?
   **Answer:** In a relational database, a table is a named collection of rows with defined columns and constraints. It represents a kind of entity or relationship, though modern databases may also support other data structures.
66. What is a row?
   **Answer:** A row is one record in a table, containing a value for each column subject to the schema and nullability rules. A primary key can identify that record uniquely.
67. What is a column?
   **Answer:** A column defines one attribute shared by rows, such as a user's email or creation date. Its type and constraints define what values are valid and help the database store and query the data.
68. Why do we need primary keys?
   **Answer:** A primary key gives each row a stable unique identity, allowing reliable updates, references, and joins. The database enforces uniqueness and non-nullability; keys can be generated IDs or meaningful natural values.
