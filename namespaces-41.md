- can assign resource quota to each namespae
- can have policies for how things behave within a namespace
- to reference a pod in a different namespace, use the format
    - <serviceName>.<namespaceName>.svc.<domainName>
    - example: when talking to the db-service, in the dev namespace, in a local cluster,
    you would use: "db-service.dev-svc-cluster.local"