- there is a field in pod definitions called nodeName which is unset by default
- the k8s scheduler scans pods for those that dont have this field set
    - applies the scheduling algorithm to apply 
- can only specify this at pod creation time
- create a binding object to mimic scheduling after the fact
    - convert this Binding to json, and send a POST request to the API with the json