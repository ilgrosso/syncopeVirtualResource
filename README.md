syncopeVirtualResource
======================

"virtual resource" proof-of-concept in Apache Syncope 1.0.X (configuration only)

## How to test
 1. clone
 1. ```mvn clean package```
 1. ```cd console```
 1. ```mvn -P embedded```

You can see now that there is a single resource named *Virtual Resource*, referring to the sole connector
instance available - *Virtual Connector*. The schema mapping is also the bare minimum required.

Such connector instance has a [CSVDir connector bundle](https://connid.atlassian.net/wiki/display/BASE/CSV+Directory) 
with basically no configuration nor capabilities.

Just create users and assign them the only resource available: you will see that everything works even
though there is no effective propagation: basically, the concept of a **virtual resource**.

## Limitations
Since Virtual Connector has no capabilities (and thus no propagation takes place), there is no mean for 
Apache Syncope to check the user status on such virtual resource: right after creation, then, when 
checking user status on associated resources, the status icon for Virtual Resource will be 'red' (no link
found).
