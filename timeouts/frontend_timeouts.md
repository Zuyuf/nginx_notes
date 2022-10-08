# Frontend Timeouts
Frontend Timeouts is what the Client talks to NGINX. For Security & Efficient use of resources.
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

