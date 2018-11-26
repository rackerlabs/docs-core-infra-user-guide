.. _servicenet:

~~~~~~~~~~~~~~~~~~~~~~~
ServiceNet in the cloud
~~~~~~~~~~~~~~~~~~~~~~~
ServiceNet is an internal, IPv4-only multi-tenant network within each
Rackspace cloud region. ServiceNet is optimized to carry traffic across servers
within your configuration
(east-west traffic).
It provides servers with no-cost access to regionalized services such as Cloud
Files, Cloud Load Balancers, Cloud Databases, and Cloud Backup.

You can configure a cloud server without ServiceNet, but Rackspace
recommends that all servers be connected to ServiceNet so that they can
access the aforementioned services.

ServiceNet is required for Windows cloud server activation and Managed
Operations support.

The networks 10.176.0.0/12 and 10.208.0.0/12 are reserved for
ServiceNet. Any servers that have ServiceNet connectivity will be
provisioned with an IP address from one of these networks.

.. include:: /_common/seealso-concepts-cloud-networks.txt
