# NGINX Notes - TL DR version
These are my notes about NGINX.   
   
   
### NGINX Basic   
1. Fireship.io 100 Seconds - [Video](https://www.youtube.com/watch?v=JKxlsvZXG7c)   
2. CodeDamn - [Video](https://www.youtube.com/watch?v=PAEDJrGJyaY)   


### NGINX Popular Use Cases  
1. Static Content   
2. Proxying Requests  
3. Load Balancing   
4. Caching   


### NGINX Fundamentals
1. Load Balancing - [Read More](./fundamentals/load_balancing.md)
1. TLS - [Read More](./fundamentals/TLS.md)


### Proxy Timeouts for Efficient Configuration
Timeouts are critical for the Security & Efficient utilization of resources.
1. Frontend Timeouts: When Client talking to NGINX - [Read More](./timeouts/frontend_timeouts.md)
2. Backend Timeouts: When NGINX talks to Backend - [Read More](./timeouts/backend_timeouts.md)


### NGINX CLI Commands
- Commonly Used Commands - [Link](./nginx_commands.md)

### NGINX HTTP Context
- Static Web Server - [Link](./http/static_server.conf)
- Layer 7 Load Balancing - [Link](./http/http_layer_7.conf)
- Layer 4 Load Balancing - [Link](./http/http_layer_4.conf)
- HTTP2 & TLSv1.3 - [Link](./http/http2_TLS.conf)

### NGINX WebSockets
- Layer 4 Load Balancing - [link](./web_socket/tcp.cfg)
- Layer 7 Load Balancing - [link](./web_socket/ws.cfg)
- Testing HTML Interface - [link](./web_socket/index.html)