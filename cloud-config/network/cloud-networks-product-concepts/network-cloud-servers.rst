.. _network-cloud-servers:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Networking considerations for cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Networks are user-defined Layer 2 networks that are fully isolated
and single-tenant, and offer users a way to securely connect their
application servers.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
IP addressing on Cloud Networks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Networks can be provisioned as either IPv4 or IPv6. Unlike PublicNet
and ServiceNet, it is possible to assign specific Cloud Networks IPs to Cloud
Servers, either at build time (by creating a port with a fixed IP) or to
an existing server (by creating a port with a fixed IP and the existing
server's UUID as device ID).

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Communicating securely between Rackspace Cloud Servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Cloud Networks is recommended for all inter-server communication. Even
though ServiceNet can also be used for server east-west (backend)
connectivity, we do not recommend ServiceNet for that purpose because,
unlike Cloud Networks, ServiceNet is multi-tenant.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You cannot NAT by using ServiceNet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To prevent spoofing,
ServiceNet is filtered on the source and destination MAC, and destination IP. Thus,
NAT will not work via ServiceNet. If you want to NAT, create a
:ref:`Gateway Instance<network-gateway-instances>`
and use Cloud Networks.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Additional Cloud Networks limits and features
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Up to 10 cloud networks are supported per region, with 250 hosts per network.
Cloud Networks can be attached to and detached from live servers, making it
possible to change the network while rebuilding Cloud Servers. Cloud
Networks also includes full support for broadcasting and multicasting
required for some clustering technologies.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Throughput in Rackspace Cloud
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Aggregate outbound bandwidth limits across all attached network
interfaces (PublicNet, ServiceNet, and Cloud Networks)
are defined for each Cloud Server based on its
performance characteristics.

By choosing a flavor class and then a specific flavor
within that class,
you can configure your Cloud Server's network speed
within the range available to it.

.. figure:: /_images/flavorclass-network-speed.png
   :alt: In the Cloud Control Panel,
         use the slider to change network speed
         and other characteristics.
         For virtual Cloud Servers, the
         "Comparison Chart" link provides a detailed comparison of
         the configuration available for each flavor.

   *In the Cloud Control Panel,
   use the slider to change network speed
   and other characteristics.
   For virtual Cloud Servers, the
   "Comparison Chart" link provides a detailed comparison of
   the configuration available for each flavor.*

You can read more about how choosing a flavor class influences
your cloud server's configuration at
:ref:`cloud-servers-flavor-class`.


.. _network-cloud-servers-working:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Working with networked Cloud Servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
As with physical servers, networked Cloud Servers are subject to
relevant limitations and requirements. Throughput is called "Network" in
the mycloud portal.

^^^^^^^^^^^^^^^
Network limits
^^^^^^^^^^^^^^^
* Only outbound throughput is limited. (Inbound traffic is not limited.)

* Throughput values listed in mycloud are theoretical maximums.
* There is no SLA for throughput.
* QoS is set across 2 sides of a bond, which means that any single layer 4
  connection will get at most 1/2 of the maximum throughput advertised in the
  portal.
* There are 2 QoS buckets - one for PublicNet and one for
  ServiceNet/Cloud Networks.
* PublicNet throughput is exactly one-half of ServiceNet/Cloud Networks
  throughput.

Host networking on Cloud Servers is redundant, with bandwidth delivered
over two separate bonded interfaces, each able to carry 50 percent of the
aggregate limit.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Practical throughput example
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
With all those caveats in mind, let's consider a theoretical cloud flavor
whose throughput is listed as 4 Gbps in the portal. The following QoS limits
apply:

.. list-table::
   :widths: 25 25 50
   :header-rows: 1

   * - Flavor throughput
     - Max/L4 connection on Cloud Networks/ServiceNet
     - Max/L4 connection on PublicNet
   * - 4 Gbps
     - 2 Gbps
     - 1 Gbps

Rackspace recommends using multiple Layer 4 connections to maximize
throughput.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Attaching or detaching networks from a server
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can attach networks to or detach networks from a Cloud Server through
the
:mycloud:`Rackspace Cloud Control Panel <>`
or an API.

Attaching any single network to or detaching it from a live server results in
a full reset of networking on the server. This reset causes a brief disruption
in network connectivity on all network interfaces on the server and
should be used with caution.

For OnMetal servers, attaching and detaching networks is not supported. Managed
Operations customers may not detach ServiceNet.

.. NOTE::
    Detaching PublicNet and ServiceNet results in a permanent loss of the
    IPs attached to those networks.


^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Programming additional network config into your Cloud Network
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can add values such as gateway IP, DNS server IPs, and static routes
into your Cloud Networks subnet and have them automatically injected
to your Cloud Servers at build time, or when they are attached.
For more details, see
"How to set up Internet access for servers without PublicNet or ServiceNet"
on the :ref:`Building servers without PublicNet or ServiceNet
<servicenet-publicnet-requirement>` page.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Adding public IPv4 addresses to Cloud Servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Rackspace offers the ability to add IPv4 addresses to Cloud Servers for
a fee.

Because of the global shortage of IPv4 address space, you might be
asked to justify your request for additional public IPv4 addresses.

Rather than assign multiple IPv4 addresses on a single Cloud Server, we
highly recommend using Cloud Load Balancers. Multiple Cloud Load Balancers
can have the same Cloud Server in their pools.

If you still want to obtain an additional IPv4 address for your server,
open a ticket through the Support section of the :mycloud:`Rackspace Cloud
Control Panel <>` to get policy details and request approval. In some
circumstances, we might ask you to provide an SSL certificate.

We cannot allocate more than four additional IPv4 addresses to a single
server. This limit gives each server a maximum capacity of five IPv4
addresses, including the originally assigned public IP address.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Rackspace Cloud, IP addressing, netranges, and gateways
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Rackspace Cloud uses static addressing. IPs are assigned as follows:

.. list-table::
   :widths: 25 25 50
   :header-rows: 1

   * - Network
     - Address range
     - Gateway
   * - PublicNet v4
     - /24 for virtual servers, /30 for OnMetal
     - First usable IP in range (.1)
   * - PublicNet v6
     - /64 for virtual servers and OnMetal
     - ``fe80::def`` for virtual servers, varies for OnMetal
   * - ServiceNet v4
     - Varies, /17 or smaller for virtual servers, /30 for OnMetal
     - First usable IP in range
   * - Cloud Networks
     - Can be IPv4 or IPv6. For v4, choose a range between /28 and /24.
     - Gateway IP and DNS Servers not defined by default. Must be defined
       for :ref:`Gateway Instances<network-gateway-instances>`
       to work properly.



.. include:: /_common/seealso-concepts-cloud-networks.txt
