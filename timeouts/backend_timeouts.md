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

### Proxy Read Timeout
- `proxy_read_timeout`
- Defines a timeout for reading a response from the proxied server. 
- The timeout is set only between two successive read operations, not for the transmission of the whole response. 
- If the proxied server does not transmit anything within this time, the connection is closed.

### Proxy Next Upstream Timeout
- `proxy_next_upstream_timeout` - Default 0.
- The 0 value turns off this limitation
- Limits the time during which a request can be passed to the next server. 


### For More Backend Timeouts
[NGINX - HTTP Proxy Module](https://nginx.org/en/docs/http/ngx_http_proxy_module.html)
