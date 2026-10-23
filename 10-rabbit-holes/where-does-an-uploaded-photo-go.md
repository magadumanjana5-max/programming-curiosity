# Rabbit Hole 5: Where Does an Uploaded Photo Go?

**Question:** When I upload a photo to Instagram, where does that photo actually go?

**Answer:** The app encodes the photo and sends it to a service, usually as an upload request. The service authenticates the user, checks limits and content, and writes the media to durable object storage. It may generate resized or compressed versions, store metadata in a database, and distribute copies through a content delivery network. The exact architecture is service-specific.

- **WHY:** Durable storage keeps media available after the upload process ends; derivatives and caches make delivery practical.
- **WHAT:** The photo's bytes, metadata, access rules, and derived versions may be stored separately.
- **HOW:** An upload API transfers bytes; backend services validate, store, process, and index them.
- **WHERE:** Data may be replicated across storage systems and geographic regions according to provider and service design.
- **WHEN:** Processing may happen synchronously or asynchronously after upload; deletion and retention policies determine its later lifecycle.
- **WHO:** The client, API service, storage system, processing workers, database, and delivery network may participate.
- **WHAT IF:** Failed uploads can be retried safely if designed for it; access controls and backups help address unauthorized access and data loss.

Explore [API requests and responses](../05-apis/request-response.md), [cloud computing](../08-cloud-and-deployment/cloud.md), and [servers](../08-cloud-and-deployment/server.md).
