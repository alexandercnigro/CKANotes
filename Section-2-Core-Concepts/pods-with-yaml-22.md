Pod definition always contains:
- apiVersion
- Kind
- metadata
- spec

- Labels go under metadata, and are allowed to be any key/value pair
- these can be used to select and/or filter pods

- Under spec, there is a "containers" header which is a list where each entry needs at least a "name" and an "image" 
