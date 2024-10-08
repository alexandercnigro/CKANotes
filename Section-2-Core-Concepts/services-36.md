3 types

- ClusterIP
    - can use these to talk to the pods in a group
    - service decides which pod in the group the requests will be routed to

- If your service is exposed through a node, you can talk to that service on the same port number using ANY node within the cluster's IP

- LoadBalancer