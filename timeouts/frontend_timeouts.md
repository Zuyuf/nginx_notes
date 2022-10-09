# Frontend Timeouts
Frontend Timeouts is what the Client talks to NGINX. The timeouts provide Security & Efficient use of resources.
#### Only Commonly used Timeouts are listed


### Client Header Timeout
- `client_header_timeout` - Default 60s.
- Defines a timeout for reading the client request header.
- If a client does not transmit the entire header within this time, the request is terminated with the 408 (Request Time-out) error.
- Mitigates _Slowloris DDoS_ Attack - [Read More](https://www.cloudflare.com/en-gb/learning/ddos/ddos-attack-tools/slowloris/)

### Client Body Timeout
- `client_body_timeout` - Default 60s.
- Defines a timeout for reading the client request body. 
- The timeout is set only for a period between two successive read operations, not for the transmission of the whole request body. 
- If a client does not transmit anything within this time, the request is terminated with the 408 (Request Time-out) error.
- Prevents Attacks: _Slowloris DDoS_

### Send Timeout
- `send_timeout` - Default 60s.
- Sets a timeout for transmitting a response to the client.
- The timeout is set only between two successive write operations, not for the transmission of the whole response.
- If the client does not receive anything within this time, the connection is closed.
- Handles Bad Requests Problems. 

### Keep Alive Timeout
- `keepalive_timeout` - Default 75s.
- The zero value disables keep-alive client connections.
- The first parameter sets a timeout during which a keep-alive client connection will stay open on the server side.
- The optional second parameter sets a value in the `“Keep-Alive: timeout=time”` response header field. Two parameters may differ

### Lingering Timeout
- `lingering_timeout` - Default 30s.
- When lingering_close is in effect, this directive specifies the maximum waiting time for more client data to arrive. 
- If data are not received during this time, the connection is closed. 
- Otherwise, the data are read and ignored, and NGINX starts waiting for more data again. 
- The “wait-read-ignore” cycle is repeated, but no longer than specified by the `lingering_time` directive.

### Resolver Timeout
- `resolver_timeout` - Default 30s.
- Sets a timeout for name resolution of the backend.
- In other words, how long NGINX will wait for an answer from the resolver (DNS)?