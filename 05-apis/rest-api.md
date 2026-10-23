# REST API

## Curiosity questions

57. What are HTTP methods?
   **Answer:** HTTP methods describe the intended operation on a resource. Their semantics help clients, servers, caches, and intermediaries reason about requests; for example, GET is intended to retrieve a representation and should not change server state.
58. Why do we have GET, POST, PUT, PATCH and DELETE?
   **Answer:** They distinguish common operations: GET retrieves, POST submits or creates subordinate actions, PUT replaces a resource, PATCH applies a partial change, and DELETE removes it. Correct method semantics improve interoperability; idempotency differs, so retries must be designed accordingly.
