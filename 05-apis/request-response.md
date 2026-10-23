# Request and Response

## Curiosity questions

53. What happens when a React application calls a Node/Python API?
   **Answer:** The browser code serializes request data and sends it over HTTP to a server endpoint. The server validates and processes it, may call a database or another service, then returns a status and data that the React app uses; the server language is hidden behind the API contract.
54. What is a request?
   **Answer:** A request is a message from a client asking a server to perform an operation or return information. It can include a method, URL, headers, and optional body; the server should validate untrusted input before using it.
55. What is a response?
   **Answer:** A response is the server's reply, usually containing a status code, headers, and optional body. The status communicates success or failure category, while the body may carry data or an error description.
56. Why do APIs commonly use JSON?
   **Answer:** JSON is a text format that is relatively small, readable, and supported across many programming languages. It is convenient for structured data, though binary formats or other encodings may be more efficient for some workloads.
59. What happens if an API takes 10 seconds to respond?
   **Answer:** The client waits, displays loading state, or times out according to its configured deadline; server resources may remain occupied too. Good systems use timeouts, monitoring, and appropriate retries with backoff, taking care not to repeat non-idempotent actions accidentally.
60. What happens if the API server is completely down?
   **Answer:** Clients cannot obtain a normal response and may see a connection error or gateway failure. Redundancy, health checks, queues, and failover can improve recovery, while clients should show a useful error and avoid unsafe retry loops.
