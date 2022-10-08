# Frontend Timeouts
Frontend Timeouts is what Client talks to NGINX. For Security & Efficient use of resources.

### Client Header Timeout
- `client_header_timeout` - Default 60s.
- Defines a timeout for reading client request header. If a client does not transmit the entire header within this time, the request is terminated with the 408 (Request Time-out) error.
- Blocks Slowloris DDos Attack - [Read More](https://www.cloudflare.com/en-gb/learning/ddos/ddos-attack-tools/slowloris/)