# Rabbit Hole 3: What Happens When You Open Google?

**Question:** When I enter `google.com`, how does my computer find another computer somewhere in the world?

**Answer:** The browser resolves the hostname through DNS to one or more IP addresses, then opens a network connection to an address and service port. For HTTPS, it negotiates TLS and verifies the site's certificate before sending an HTTP request. Routers forward packets between networks; Google's infrastructure routes the request to a suitable service, which sends a response back over the connection.

- **WHY:** Names are easier to remember than numeric network addresses, and packets need routable destinations.
- **WHAT:** DNS records, IP addresses, ports, TLS, and HTTP work together to reach a web service securely.
- **HOW:** A resolver finds an address; network routing carries packets; the browser and server exchange protocol messages.
- **WHERE:** The request crosses local networks, Internet providers, and data-center infrastructure.
- **WHEN:** DNS may be skipped if a valid cached answer exists; addresses and routes can change.
- **WHO:** The browser, DNS resolvers, network operators, routers, and destination service participate.
- **WHAT IF:** If DNS, the route, TLS validation, or the service fails, the browser reports a lookup, connection, security, or server error.

Continue with [DNS](../04-internet/dns.md), [IP addresses](../04-internet/ip.md), [HTTP](../04-internet/http.md), and [HTTPS](../04-internet/https.md).
