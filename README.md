# This application is an example of nginx load balancer
# Load balancer directs network traffic through different backend servers

# In this project i represent this concept by displaying ip address of current backend server that handles request
# I created a python program which displays the local ip address of the machine

# 3 containers, that act as a flask backend server.

# 1 nginx container which acts as load balancer

# configured the nginx file to navigate traffic to each of these servers using the Round Robin method: Requests are distributed evenly across the servers.
# Used docker compose to create the network between diffrent containers.

