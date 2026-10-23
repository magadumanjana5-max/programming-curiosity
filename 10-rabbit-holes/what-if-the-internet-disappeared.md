# Rabbit Hole 10: What If the Internet Disappeared?

**Question:** If the Internet disappeared tomorrow, which parts of your application would still work?

**Answer:** Work that is entirely local—such as opening installed software, reading cached files, or editing offline data—could continue. Features requiring remote APIs, cloud databases, authentication services, updates, or other networked systems would fail or become stale. Applications with offline modes may queue changes locally and synchronize later, if they were designed to do so.

- **WHY:** Applications depend on networks to reach remote services and synchronize shared data.
- **WHAT:** The Internet is a global network of interconnected networks; it is not the same as every local network or offline capability.
- **HOW:** Local code can run without external connectivity, but remote requests cannot complete while routes are unavailable.
- **WHERE:** Data and services on the device or local network may remain reachable; distant services may not.
- **WHEN:** Cached and offline features work until they need fresh data or a network-dependent action.
- **WHO:** Users, service operators, network providers, and application designers are affected.
- **WHAT IF:** Design for offline use where it matters: cache safely, communicate stale state, queue changes, and resolve sync conflicts.

Explore [servers](../08-cloud-and-deployment/server.md), [cloud computing](../08-cloud-and-deployment/cloud.md), and [the Internet](../04-internet/dns.md).
