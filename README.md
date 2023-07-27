# NGINX Load Balancer with Flask Backend Servers

This repository demonstrates a simple yet effective load balancing setup using NGINX and Flask backend servers. When a request is made to the load balancer, it directs the traffic to one of the Flask backend servers, which in turn displays the IP address of the machine that handled the request.

## Architecture

- **NGINX Load Balancer**: An NGINX container that acts as a load balancer to evenly distribute incoming requests to backend Flask servers using the Round Robin method.
  
- **Flask Backend Servers**: Three separate containers running a Flask application that displays the local IP address of the machine.

## Features

- Simple demonstration of load balancing concept using NGINX.
- Round Robin load balancing method for even request distribution.
- Each backend server displays its IP address, providing clear evidence of load balancing in action.
- Use of Docker Compose for creating the necessary network among containers.

## Prerequisites

Ensure you have the following installed:

- Docker
- Docker Compose

## Getting Started

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yuvalcoren/loadbalancer.git
   cd loadbalancer
   ```

2. **Build and Start the Containers**

   ```bash
   docker-compose up --build
   ```

3. **Access the Load Balancer**

   Open your browser and navigate to `http://localhost:9090`. Refresh the page multiple times to see the IP address change as the request gets directed to different backend servers.

## Clean Up

To stop and remove the containers:

```bash
docker-compose down
```
