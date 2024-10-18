- ensures pods are hosted on particular nodes
- uses labels and selectors in more complex ways to assign the pods to particular nodes
- in your pod config, use
 ```
 affinity:
    nodeAffinity:
    requiredDuringSchedulingIgnoredDuringExecution:
        nodeSelectorTerms:
        - matchExpressions:
            - key: size
                operator: Exists|In|NotIn|etc
                values:
                - Large
                - Medium
```
- if node affinity type is:
    - Available
        - changes to node affinity or labels will not affect already scheduled pods in these cases
            - requiredDuringSchedulingIgnoredDuringExecution
                - if a node matching the criteria is not found, pod isnt scheduled
            - preferredDuringSchedulingIgnoredDuringExecution
                - if a node matching the criteria is not found, pod is scheduled on another available node
    - Planned
        - requiredDuringSchedulingRequiredDuringExecution