# Authentication

## Curiosity questions

71. How does a website know who you are after login?
   **Answer:** The server verifies the login credentials and establishes a session, often represented by a random session ID in a secure cookie or by a token. Later requests present that proof, which the server validates and associates with an account; it should expire and be protected against theft.
72. Where is your password stored?
   **Answer:** A well-designed service stores a salted password hash produced by a purpose-built password-hashing algorithm, not the original password. The hash and salt are kept in protected account storage; plaintext should not be recoverable by the service.
73. Why shouldn’t passwords be stored as plain text?
   **Answer:** A database breach would immediately expose users' passwords, including passwords they may have reused elsewhere. Slow salted password hashing makes offline guessing substantially harder; encryption alone is not a substitute because the service would need a decryption key.
79. What is a token?
   **Answer:** A token is a piece of data representing a credential or authorization claim. A bearer token grants access to whoever possesses it, so it must be protected, scoped, validated, and given an appropriate lifetime; tokens can be opaque or cryptographically signed.

## Rabbit hole

- [How does a login request travel from your phone to the server and return “Login successful”?](../10-rabbit-holes/how-a-login-works.md)
