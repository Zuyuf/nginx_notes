# TLS
TLS stands for Transport Layer Security.

- It is a way to establish end-to-end encryption.
- Asymmetric Encryption is initially used to exchange the Symmentric Key.
- Symmentric Encryption is then used for communication (Client & Server has the same key).
- Server needs to authenticate themselves by supplying a certificate signed by certificate authority. 


## TLS Termination 
When L7 Load Balancer is Setup then TLS termination is required to Decrypt & read data.

### Approach 1
- NGINX has TLS (eg: HTTPS) backend doesn't (eg: HTTP).
- NGINX terminates TLS and decrypts and send unencrypted data to Backend.

### Approach 2
- NGINX is TLS and backend is also TLS (eg: HTTPS).
- NGINX terminates TLS, decrypts, optionally rewrite and then re-encrypt the content to the backend.
- NGINX can look at the L7 data, re-write headers, cache but needs to share the backend certificate or at least has its own. 


## TLS Passthrough
- Backend is TLS
- NGINX just proxies/streams the packets directly to the backend.  
- The TLS handshake is forwarded all the way to the backend.  
- Just like a tunnel.  
- No caching, L4 check only, but more secure, NGINX doesn’t need
the backend certificate.   

