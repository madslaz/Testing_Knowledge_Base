## Enumeration & Brute Force
- Basic authentication: Straightforward login method which only requires a username and password. Easy to implement and manage on devices with limited processing capabilities.
  - Network devices, like routers, typically use basic authentication to control access to their administrative interfaces.
  - Session management and user tracking is not required or is managed differently.
  - Defined in RFC 7617, the credentials (username and password) should be transported as a base64-encoded string within the HTTP Authorization header.
    - Straightforward but not secure over non-HTTPS connection.  

`hydra -l admin -P /usr/share/wordlists/SecLists/Passwords/Common-Credentials/500-worst-passwords.txt -f 10.10.192.40  http-get /labs/basic_auth` - https://www.kali.org/tools/hydra/
- [`waybackurls`](https://github.com/tomnomnom/waybackurls) to dump all links saved in Wayback Machine.

## Session Management
- Attributes that may by added to cookie:
  - **Secure**: Indicates to browser that cookie may only be transmitted over verified HTTPS channels. If there are certificate errors or HTTP is used, the cookie value will not be transmitted.
  - **HTTPOnly**: Indicates to browser that the cookie value may not be read by client-side JavaScript.
  - **Expire**: Indicates to the browser when a cookie value will no longer be valid and should be removed.
  - **SameSite**: Indicates to the browser whether the cookie may be transmitted in cross-site requests to help protect against CSRF attacks.
    - SameSite="Lax" allows the cookies to be sent on some cross-site requests, while "Strict" never allows cookies to be sent on a cross-site request.
- Token-based session management is a relatively new concept. Instead of using browser's automatic cookie management featuries, it relies on client-side code for the process.
  - After authentication, the web application provides a token within the request body. Using client-side JavaScript code, this token is then stored in the browser's LocalStorage.
  - When a new request is made, JavaScript code must load the token from storage and attach it as a header.
  - More common types of tokens is JSON Web Tokens (JWT), which is passed through the `Authorization: Bearer` header. 

|Cookie-Session Management|Token-Based Session Management|
|-----------|-----------|
|Cookie is auto sent by browser with each request|Token has to be submitted as a header with each request using client-side JS|
|Cookie attributes can be used to enhance browser's protection of cookie|Tokens do not have automatic security protections enforced and should, therefore, be safeguarded against disclosures|
|Cookies can be vulnerable to conventional client-side attacks such as CSRF, where the browser is tricked into making a request on behalf of the user|As token is  not automatically added to any request and cannot be read from LocalStorage by other domains, conventional client-side attacks, such as CSRF, are blocked|
|As cookies are locked to a specific domain, it can be difficult to use them securely in decentralized web applications|Tokens work well in decentralized web applications, as they are managed through JS and can often contain all the information to verify the token itself|
