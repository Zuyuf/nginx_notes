# Backend Timeouts
Backend Timeouts are when the NGINX talks to the Backend. The timeouts provide Security & Efficient use of resources.

#### Only Commonly used Timeouts are listed

### Proxy Connect Timeout
- `proxy_connect_timeout` - Max 75s.
- The timeout cannot usually exceed 75 seconds
- Timeout for establishing a connection with a proxied server.

### Proxy Send Timeout
- `proxy_send_timeout`
- Sets a timeout for transmitting a request to the proxied server. 
- The timeout is set only between two successive write operations, not for the transmission of the whole request. 
- If the proxied server does not receive anything within this time, the connection is closed.
