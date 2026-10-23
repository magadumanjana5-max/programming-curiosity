# Servers and Deployment

## Curiosity questions

91. Where does your application actually run after deployment?
   **Answer:** It runs on physical computers in a data center, accessed directly or through virtual machines, containers, or managed platforms. The deployment configuration determines which machines and regions host it and how users reach it.
95. What is a server?
   **Answer:** A server is a program or computer that provides a service to clients over a network. The term describes a role: one machine can run many server processes, and a server process can run across multiple machines.
98. What happens when a server crashes?
   **Answer:** Requests to that instance may fail or time out, and in-memory state can be lost. Load balancers and health checks can route around it, while supervisors restart it; durable storage and replicated systems help preserve data and service.
