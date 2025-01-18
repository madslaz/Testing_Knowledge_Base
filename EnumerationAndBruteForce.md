## Enumeration & Brute Force
- Basic authentication: Straightforward login method which only requires a username and password. Easy to implement and manage on devices with limited processing capabilities.
  - Network devices, like routers, typically use basic authentication to control access to their administrative interfaces.
  - Session management and user tracking is not required or is managed differently.
  - Defined in RFC 7617, the credentials (username and password) should be transported as a base64-encoded string within the HTTP Authorization header.
    - Straightforward but not secure over non-HTTPS connection.  
