.. _servicenet:

~~~~~~~~~~~~~~~~~~~~~~~
ServiceNet in the cloud
~~~~~~~~~~~~~~~~~~~~~~~
ServiceNet is an internal, IPv4-only multi-tenant network within each
Rackspace Cloud region. ServiceNet is optimized to carry traffic across servers 
within your configuration 
(east-west traffic).
It provides servers with access to regionalized services such as Cloud
Files, Cloud Load Balancers, Cloud Databases, and Cloud Backup at no
cost.

You can configure a Cloud Server without ServiceNet, but Rackspace
recommends that all servers be connected to ServiceNet so that they can
access the aforementioned services.

ServiceNet is required for Windows Cloud Server activation.

The networks 10.176.0.0/12 and 10.208.0.0/12 are reserved for
ServiceNet. Any servers that have ServiceNet connectivity will be
provisioned with an IP address from one of these networks.
