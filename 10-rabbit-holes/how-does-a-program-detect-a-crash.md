# Rabbit Hole 8: How Does a Program Detect a Crash?

**Question:** How does a program know that another program has crashed?

**Answer:** A parent process can receive an operating-system notification when a child exits and inspect its exit status. For a remote service, a client or supervisor cannot directly see the other process; it infers health from timeouts, failed connections, heartbeats, or health checks. A timeout means “no response in time,” not proof of the exact cause.

- **WHY:** Detection lets software report failures, restart workers, or route work elsewhere.
- **WHAT:** A crash is an unexpected termination or loss of service, distinguished from a normal shutdown by status or behavior.
- **HOW:** Local process APIs, heartbeats, health probes, and timeouts provide evidence of failure.
- **WHERE:** Local detection uses OS process state; remote detection happens across a network boundary.
- **WHEN:** Checks run periodically or when work is attempted; overly frequent checks waste resources.
- **WHO:** The operating system, parent process, monitoring system, or client may detect the failure.
- **WHAT IF:** A slow network looks like a crash? Use bounded timeouts and resilient recovery; avoid assuming every missed heartbeat means permanent failure.

Explore [processes](../03-how-programs-run/process.md), [threads](../03-how-programs-run/threads.md), and [servers](../08-cloud-and-deployment/server.md).
