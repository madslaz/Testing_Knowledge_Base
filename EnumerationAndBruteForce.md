## Enumeration & Brute Force
- Basic authentication: Straightforward login method which only requires a username and password. Easy to implement and manage on devices with limited processing capabilities.
  - Network devices, like routers, typically use basic authentication to control access to their administrative interfaces.
  - Session management and user tracking is not required or is managed differently.
  - Defined in RFC 7617, the credentials (username and password) should be transported as a base64-encoded string within the HTTP Authorization header.
    - Straightforward but not secure over non-HTTPS connection.  

`hydra -l admin -P /usr/share/wordlists/SecLists/Passwords/Common-Credentials/500-worst-passwords.txt -f 10.10.192.40  http-get /labs/basic_auth` - https://www.kali.org/tools/hydra/
- `waybackurls` to dump all links saved in Wayback Machine.

## Session Management
- Attributes that may by added to cookie:
  - **Secure**: Indicates to browser that cookie may only be transmitted over verified HTTPS channels. If there are certificate errors or HTTP is used, the cookie value will not be transmitted.
  - **HTTPOnly**: Indicates to browser that the cookie value may not be read by client-side JavaScript.
  - **Expire**: Indicates to the browser when a cookie value will no longer be valid and should be removed.
  - **SameSite**: Indicates to the browser whether the cookie may be transmitted in cross-site requests to help protect against CSRF attacks.
    - SameSite="Lax" allows the cookies to be sent on some cross-site requests, while "Strict" never allows cookies to be sent on a cross-site request. 

