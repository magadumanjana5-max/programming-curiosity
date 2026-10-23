# Scaling

## Curiosity questions

92. What happens when 1 user uses your application?
   **Answer:** A client sends a request to an application server, which may run code and read or write data before responding. Even one user depends on a chain of components—device, network, server, and often database—any of which can fail.
93. What changes when 1 million users use it?
   **Answer:** Traffic, concurrent work, storage, and failure probability rise, so bottlenecks appear in compute, databases, networks, and operations. Teams measure load and scale horizontally or vertically, cache suitable data, partition work, and design for graceful degradation.
94. Why can’t we simply buy one huge computer?
   **Answer:** A single machine has practical limits in cost, capacity, network throughput, and maintenance, and it remains a single point of failure. Multiple machines can distribute load and improve resilience, though coordination and distributed failures add complexity.
99. How does Netflix/YouTube/Instagram handle millions of users?
   **Answer:** Large services combine many techniques: distributed application servers, caches, databases, queues, content delivery networks, replication, monitoring, and automated deployment. Exact architectures are proprietary and change over time; the common principle is to distribute load and avoid relying on one machine.
100. If you had to build WhatsApp from scratch, what would you need?
   **Answer:** At minimum: identity and authentication, contact and messaging APIs, durable message storage, delivery queues, real-time connections, encryption, media storage, notifications, abuse prevention, backups, and monitoring. A production service also needs scalable infrastructure, privacy and security design, reliability engineering, and a team to operate it.

## Rabbit hole

- [How can millions of people use the same application at the same time?](../10-rabbit-holes/how-does-software-scale.md)
