- taints and tolerations are generally used to exclude certain pods from being placed on certain nodes
    - this does not guarantee those pods will end up on a specific node, only that they WONT end up on a specific node
- node affinity is used to ensure certain pods are placed on certain nodes
    - this does not guarantee that other pods WONT end up on these nodes, only that certain pods WILL be placed on these nodes
- these concepts can be used in combination to ensure certain nodes are dedicated to certain pods