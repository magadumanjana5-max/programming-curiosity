# Rabbit Hole 9: How Do Programming Languages Communicate?

**Question:** If Python, JavaScript and Java are completely different languages, how can they communicate with each other?

**Answer:** They agree on a boundary and a shared representation. A browser can send JSON over HTTP to a Python or JavaScript service; programs can also exchange files, use a database, or call native libraries through a foreign-function interface. Each language implements the protocol or interface on its own side.

- **WHY:** A stable boundary lets teams build components independently and choose tools suited to each task.
- **WHAT:** The contract defines operations, data formats, errors, and compatibility expectations.
- **HOW:** Serialization converts values to a shared format; protocols transport them; receiving code parses and validates them.
- **WHERE:** Communication may cross a network, process boundary, runtime, or native-library interface.
- **WHEN:** Use a network API for independently deployed services; use an in-process interface when tight integration and latency matter.
- **WHO:** Producers and consumers of the interface must follow the same contract.
- **WHAT IF:** The contract changes or one service is unavailable? Versioning, validation, timeouts, and backwards compatibility help contain the impact.

Explore [language comparisons](../09-language-comparisons/python-vs-javascript-vs-java.md) and [APIs](../05-apis/what-is-api.md).
