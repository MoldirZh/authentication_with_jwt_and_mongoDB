# jwt

## Two REST routes:

- The first route issues a pair of Access, Refresh tokens for the user with the identifier (GUID) specified in the request parameter
- The second route performs a Refresh operation on a pair of Access, Refresh tokens

## Description

- Access token JWT type, SHA512 algorithm, it is strictly forbidden to store in the database.
- Refresh token is an arbitrary type, base64 transfer format, stored in the database exclusively as a bcrypt hash, must be protected from client-side modification and reuse attempts.
- Access, Refresh tokens are mutually related, the Refresh operation for an Access token can only be performed by the Refresh token that was issued along with it.
