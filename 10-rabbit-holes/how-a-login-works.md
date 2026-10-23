# Rabbit Hole 4: How a Login Works

**Question:** When I click Login, how does my password travel from my phone to the server and come back as “Login successful”?

**Answer:** The app sends credentials to the service over HTTPS. The server validates the input, looks up the account, and compares a password hash computed with the stored salt and password-hashing algorithm. On success it creates a session or issues a token; the client stores the resulting credential safely and presents it on later requests. The server checks it and its permissions each time. A real system should also use rate limits, secure recovery, and protections against stolen credentials.

- **WHY:** Authentication establishes an account identity; authorization decides what that identity may do.
- **WHAT:** Credentials prove identity initially; a session cookie or token carries proof to later requests.
- **HOW:** TLS protects traffic in transit, password hashing supports verification, and session/token validation recognizes later requests.
- **WHERE:** Password verification occurs on the service; session state may be held server-side or represented by a signed token.
- **WHEN:** Login occurs when credentials are submitted; sessions expire, are revoked, or require reauthentication.
- **WHO:** The user, client app, network, identity service, and account store are involved.
- **WHAT IF:** Wrong credentials should not reveal sensitive account details; stolen tokens should be revocable or expire, and suspected compromise should trigger protective recovery.

Continue with [authentication](../07-security/authentication.md), [authorization](../07-security/authorization.md), [HTTPS](../04-internet/https.md), and [API requests and responses](../05-apis/request-response.md).
