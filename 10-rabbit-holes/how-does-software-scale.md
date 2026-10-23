# Rabbit Hole 6: How Does Software Scale?

**Question:** How can millions of people use the same application at the same time?

**Answer:** Large applications distribute requests across many server instances and use caches, queues, databases, and content delivery networks to avoid making one machine handle everything. Teams monitor bottlenecks, add capacity, partition workloads where needed, and design for partial failure. “Millions of users” does not mean all users make a request at the exact same instant.

- **WHY:** Distribution increases capacity and availability beyond a single machine's limits.
- **WHAT:** Scaling is the ability to handle changing demand while maintaining acceptable performance and reliability.
- **HOW:** Load balancing, replication, caching, asynchronous processing, and capacity planning share the work.
- **WHERE:** Components may run across machines, zones, and regions in data centers or cloud infrastructure.
- **WHEN:** Systems scale in response to measured or anticipated demand, while avoiding unnecessary cost.
- **WHO:** Software, infrastructure, and operations teams build and monitor the service.
- **WHAT IF:** A server or region fails? Redundancy and health checks can route around it, but state and dependencies must also be resilient.

Explore [scaling](../08-cloud-and-deployment/scaling.md), [servers](../08-cloud-and-deployment/server.md), and [cloud computing](../08-cloud-and-deployment/cloud.md).
