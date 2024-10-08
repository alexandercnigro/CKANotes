- responsible for deciding which pod goes on which node
- does NOT PLACE the pod on the node, only makes the DECISION
- how does it do this?
    - filters out nodes that dont fit profile for the pod
        - for example, dont meet CPU and memory reuqirements
    - ranks the remaining nodes on a scale of 1-10
        - bases this on many things, forexample, how many resources would be left on the node
        after scheduling the pod
- can use kubeadm to interact with kubescheduler
- this is deployed as a pod on the kube-system namespace