# Load Balancing
To distribute the load among multiple servers.


### Terminologies
- Layer 4/7 refers to OSI Layers - [Read More](https://www.cloudflare.com/en-gb/learning/ddos/glossary/open-systems-interconnection-model-osi/)


### 2 types of Load Balancing in NGINX
1. Layer 4 (TCP/IP) Load Balancing 
2. Layer 7 (HTTP, gRPC, etc) Load Balancing 


## Layer 4 Load Balancing
only TCP/IP is accessible nothing about the Application Layer (Layer 7).
- Source IP & Port
- Destination IP & Port
- Also can do simple Packet Inspections such as SYN/TLS hello
- Useful when NGINX doesn’t
understand the protocol (MySQL database protocol)
- Using `stream` context it becomes a layer 4 proxy 


## Layer 7 Load Balancing
Have access to a lot more information bcoz this is in the Application Layer (Layer 7).
- Requires Description
- Knowledge of What the client is accessing
- Useful when NGINX wants to share
backend connections and cache results
- Using `HTTP` context it becomes a layer 7 proxy