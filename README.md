syncopeVirtualResource
======================

"virtual resource" proof-of-concept in Apache Syncope 1.0.X (configuration only)

## How to test
 1. clone
 1. ```mvn clean package```
 1. ```cd console```
 1. ```mvn -P embedded```

You can see now that there is a single resource named *Virtual Resource*, referring to the sole connector
instance available - *Virtual Connector*.

Such connector instance has a [CSVDir connector bundle](https://code.google.com/p/connid/wiki/CSVDirectory) 
with basically no configuration nor capabilities.

Just create users and assign them the only resource available: you will see that everything works even
though there is no effective propagation: basically, the concept of a **virtual resource**.