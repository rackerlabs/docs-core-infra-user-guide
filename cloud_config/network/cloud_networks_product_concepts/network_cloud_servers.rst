.. _network_cloud_servers:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Networks: internal-use connections for Cloud Servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Networks are user-defined L2 networks that are fully isolated,
single-tenant, and offer users a means to securely connect their
application servers.

Cloud Networks can be provisioned as either IPv4 or IPv6.

Cloud Networks are recommended for all inter-server communication. Even
though ServiceNet can also be used for server east-west (backend)
connectivity, ServiceNet is not recommended for that purpose since,
unlike Cloud Networks, ServiceNet is multi-tenant.

Up to 10 cloud networks are supported per region with 250 hosts/network.
Cloud Networks can be attached and detached from live servers, making it
possible to change the network while rebuilding Cloud Servers. Cloud
Networks also includes full support for broadcasting and multicasting
required for some clustering technologies.

Aggregate outbound bandwidth limits across all attached network
interfaces (PublicNet, ServiceNet, Cloud Networks) 
are defined for each Cloud Server based on its 
performance characteristics:

* Performance1:

   * Performance1-1: 200Mbps

   * Performance1-2: 400Mbps

   * Performance1-4: 800Mbps

   * Performance1-8: 1,600Mbps

* Performance2:

   * Performance2-15: 1.250Mbps

   * Performance2-30 2,500Mbps

   * Performance2-60: 5,000Mbps

   * Performance2-90: 7,500Mbps

   * Performance2-120: 10,000Mbps

.. _network_cloud_servers-working:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Working with networked Cloud Servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
As with physical servers, networked Cloud Servers are subject to
relevant limitations and requirements.

Network limits
^^^^^^^^^^^^^^
Outbound PublicNet bandwidth is limited to 50% of the aggregate limit.

No such limits are applicable to ServiceNet or Cloud Networks.

Inbound PublicNet traffic is not limited.

Host networking on Cloud Servers is redundant, with bandwidth delivered
over two separate bonded interfaces, each able to carry 50% of the
aggregate limit.

Rackspace recommends using multiple Layer 4 connections to maximize
throughput.

Attaching or detaching networks from a server
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can attach or detach networks from a Cloud Server through
the 
`Rackspace Cloud Control Panel <https://mycloud.rackspace.com/>`__
or an API.

Attaching or detaching any single network from a live server results in
a full reset of networking on the server. This causes a brief disruption
in network connectivity on all network interfaces on the server and
should be used with caution.

For OnMetal servers, attaching and detaching networks is not supported.

Building servers without PublicNet or ServiceNet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
If a server is built without PublicNet or ServiceNet, it cannot access
certain Rackspace products and services.

As shown in the figure below, PublicNet and ServiceNet are essential to
a fully-functional cloud configuration. PublicNet provides a Cloud
Server with access to the Web as well as Cloud Monitoring, Cloud Backup,
Managed Cloud Support, and operating system updates. ServiceNet provides
a Cloud Server with access to Cloud Databases, Cloud Load Balancers,
Cloud Files, Cloud Backup, RackConnect, and Windows activation.

.. figure:: /_images/CloudServerNetworkRemovalResults.png
   :alt: PublicNet and ServiceNet enable full Cloud Servers functionality.
   
   *PublicNet and ServiceNet enable full Cloud Servers functionality.*

Adding IPv4 addresses to Cloud Servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Rackspace offers the ability to add IPv4 addresses to Cloud Servers for
a fee.

Due to the global shortage of IPv4 address space, Rackspace only offers
additional IPv4 addresses for the following purposes:

* SSL (Secure Sockets Layer) on Cloud Servers

* NAT (Network Address Translation) on a Brocade Vyatta vRouter

If you wish to obtain an additional IPv4 address for your server, please
open a ticket through the Support section of the \ `Rackspace Cloud
Control Panel <https://mycloud.rackspace.com/>`__ to get policy details
and request approval.

After you are approved for an additional IPv4 address to support SSL on
a Cloud Server, we will ask you to provide the following information:

* The name of the server for which you would like to add the IP address.

* Permission to restart the network service so that Rackspace Support
  can configure the IP address. We may also ask you to indicate an
  acceptable maintenance window during which we can perform the change.

* The SSL certificate. The certificate must have been signed by a valid
  Certificate Authority; self-signed certificates are not accepted.

After you are approved for an additional IPv4 address to support NAT on
a Brocade Vyatta Router, we will ask you to provide the following
information:

* Confirmation that you intend to use the additional IPV4 address for
  the purpose of NAT.

* Permission to restart the network service so that Rackspace Support
  can configure the IP address. We may also ask you to indicate an
  acceptable maintenance window during which we can perform the change.

We cannot allocate more than 4 additional IPv4 addresses to a single
Cloud Server or to a Brocade Vyatta vRouter. This gives each Cloud
Server or Brocade Vyatta vRouter a maximum capacity of five (5) IPv4
addresses, including the originally-assigned public IP address.
