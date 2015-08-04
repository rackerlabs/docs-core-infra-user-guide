.. _network-cloud-servers:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Networking considerations for cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Networks are user-defined Layer 2 networks that are fully isolated
and single-tenant, and offer users a way to securely connect their
application servers.

Cloud Networks can be provisioned as either IPv4 or IPv6.

Cloud Networks is recommended for all inter-server communication. Even
though ServiceNet can also be used for server east-west (backend)
connectivity, we do not recommend ServiceNet for that purpose because,
unlike Cloud Networks, ServiceNet is multi-tenant.

Up to 10 cloud networks are supported per region, with 250 hosts per network.
Cloud networks can be attached to and detached from live servers, making it
possible to change the network while rebuilding cloud servers. Cloud
Networks also includes full support for broadcasting and multicasting
required for some clustering technologies.

Aggregate outbound bandwidth limits across all attached network
interfaces (PublicNet, ServiceNet, and Cloud Networks)
are defined for each cloud server based on its
performance characteristics.

By choosing a flavor class and then a specific flavor
within that class,
you can configure your cloud server's network speed
within the range available to it.

.. figure:: /_images/flavorclass-network-speed.png
   :alt: In the Cloud Control Panel,
         use the slider to change network speed
         and other characteristics.
         For virtual cloud servers, the
         "Comparison Chart" link provides a detailed comparison of
         the configuration available for each flavor.

   *In the Cloud Control Panel,
   use the slider to change network speed
   and other characteristics.
   For virtual cloud servers, the
   "Comparison Chart" link provides a detailed comparison of
   the configuration available for each flavor.*

You can read more about how choosing a flavor class influences
your cloud server's configuration at
:ref:`cloud-servers-flavor-class`.


.. _network-cloud-servers-working:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Working with networked cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
As with physical servers, networked cloud servers are subject to
relevant limitations and requirements.

Network limits
^^^^^^^^^^^^^^
Outbound PublicNet bandwidth is limited to 50 percent of the aggregate limit.

No such limits are applicable to ServiceNet or Cloud Networks.

Inbound PublicNet traffic is not limited.

Host networking on cloud servers is redundant, with bandwidth delivered
over two separate bonded interfaces, each able to carry 50 percent of the
aggregate limit.

Rackspace recommends using multiple Layer 4 connections to maximize
throughput.

Attaching or detaching networks from a server
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can attach networks to or detach networks from a cloud server through
the
:mycloud:`Rackspace Cloud Control Panel <>`
or an API.

Attaching any single network to or detaching it from a live server results in
a full reset of networking on the server. This reset causes a brief disruption
in network connectivity on all network interfaces on the server and
should be used with caution.

For OnMetal servers, attaching and detaching networks is not supported.

Building servers without PublicNet or ServiceNet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
If a server is built without a PublicNet or ServiceNet network,
it cannot access
certain Rackspace products and services.

As shown in the following figure, PublicNet and ServiceNet are essential to
a fully functional cloud configuration.

.. figure:: /_images/cloudservernetworkremovalresults.png
   :alt: PublicNet and ServiceNet enable full Cloud Servers functionality.

   *PublicNet and ServiceNet enable full Cloud Servers functionality.*

* PublicNet provides a server with access to the Web as well
  as Cloud Monitoring, Cloud Backup, Managed Cloud Support, and
  operating system updates.

* ServiceNet provides a server with access to Cloud Databases,
  Cloud Load Balancers, Cloud Files, Cloud Backup,
  RackConnect, and Windows activation.

Adding IPv4 addresses to cloud servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Rackspace offers the ability to add IPv4 addresses to cloud servers for
a fee.

Because of the global shortage of IPv4 address space, Rackspace offers
additional IPv4 addresses only for the following purposes:

* SSL (Secure Sockets Layer) on Cloud Servers

* NAT (Network Address Translation) on a Brocade Vyatta vRouter

If you want to obtain an additional IPv4 address for your server,
open a ticket through the Support section of the :mycloud:`Rackspace Cloud
Control Panel <>` to get policy details and request approval.

After you are approved for an additional IPv4 address to support SSL on
a cloud server, we will ask you to provide the following information:

* The name of the server for which you want to add the IP address.

* Permission to restart the network service so that Rackspace Support
  can configure the IP address. We might also ask you to indicate an
  acceptable maintenance window during which we can perform the change.

* The SSL certificate. The certificate must have been signed by a valid
  Certificate Authority. Self-signed certificates are not accepted.

After you are approved for an additional IPv4 address to support NAT on
a Brocade Vyatta Router, we will ask you to provide the following
information:

* Confirmation that you intend to use the additional IPV4 address for
  the purpose of NAT.

* Permission to restart the network service so that Rackspace Support
  can configure the IP address. We might also ask you to indicate an
  acceptable maintenance window during which we can perform the change.

We cannot allocate more than four additional IPv4 addresses to a single
server or to a Brocade Vyatta vRouter. This limit gives each
server or router a maximum capacity of five IPv4
addresses, including the originally assigned public IP address.
