# Authorization and Web Security

## Curiosity questions

76. What happens if someone changes an API request?
   **Answer:** The server must treat every request as untrusted and independently validate its fields and permissions. Changing a price, account ID, or role in the client should not grant access; authorization decisions must use trusted server-side identity and policy.
77. What is CORS?
   **Answer:** Cross-Origin Resource Sharing is a browser-enforced policy in which a server's HTTP headers specify which web origins may read its responses. It is not authentication and does not stop non-browser clients; servers still need authorization and input validation.
78. How does a server know whether you are authorized?
   **Answer:** It authenticates the requester, obtains trusted identity or claims, then checks an access policy for the requested action and resource. Authorization should be checked on every relevant request, not assumed because a button is hidden in the interface.
80. How can one careless line of code expose millions of users?
   **Answer:** A single missing permission check, unsafe query, leaked secret, or overly broad data response can affect every user handled by that code path. Impact depends on deployment and data access; least privilege, code review, tests, monitoring, and incident response reduce the risk.
