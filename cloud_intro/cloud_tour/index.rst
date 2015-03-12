Touring the managed cloud, service by service
---------------------------------------------
The managed cloud is more than a virtualized representation of physical
computing resources, but thinking of it that way may help you understand
how so many different services combine to support your workload. Just as
if you had a fixed configuration of physical computing equipment, the
services that provide you with flexible computing in the cloud must
deliver processing power (Cloud Servers) in reusable patterns (Cloud
Images), connectable as an internal network (Cloud Networks) and
expandable to large storage sizes (Cloud Block Storage). We consider
these four services to be the core infrastructure of our managed cloud;
the core infrastructure is the focus of this guide.

Other services provide additional functions such as authentication
(Cloud Identity), recoverability (Cloud Backup), long-term storage
(Cloud Files) and databases (Cloud Databases, Cloud Big Data, Object
Rocket), connections to public-facing networks (Cloud CDN, Cloud DNS,
Cloud Load Balancers) and dedicated hardware (RackConnect), observation
of activity (Cloud Monitoring, Cloud Metrics, Cloud Feeds), and
automated installation (Cloud Orchestration) and reconfiguration (Auto
Scale). These services work well with the core infrastructure and with
each other. They are not the primary focus of this guide, but we'll
mention them when they are relevant.

In other Rackspace resources such as the 
`Cloud Control Panel <https://mycloud.rackspace.com/>`__
and the 
`Knowledge Center <http://www.rackspace.com/knowledge_center/>`__,
you should notice that Rackspace cloud products
are grouped so that closely-related products are likely to be discussed together. 
We follow that convention here, introducing several categories of cloud products 
available as services in the Rackspace cloud.

Contents:
 
.. toctree:: 
   :maxdepth: 2 
 
   compute_services/index 
   network_services/index
   storage_services/index
   data_services/index
   application_services/index
   support_services/index


Compute services
----------------

Cloud Servers at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~

★ core infrastructure: more at Cloud Servers: flexible computing power

 open-source roots: OpenStack Nova

 product overview: http://www.rackspace.com/cloud/servers

$ PAY only for what you use

xxxxxxx

get details from

https://one.rackspace.com/display/productweb/Virtual+Cloud+Servers

get details from
https://one.rackspace.com/display/productweb/OnMetal+Cloud+Servers

Cloud Networks at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~

Cloud Networks enables customers to create and manage secure, isolated
networks in the cloud.  These networks are fully single tenant, and
customers have complete control over the network topology, IP addressing
(IPv4 or IPv6), and which Cloud Servers are connected to the network.

Typical use cases
^^^^^^^^^^^^^^^^^

**Security**

Get fully isolated, single-tenant Layer 2 networks designed to securely
transfer sensitive information between Cloud Servers located in the same
region.

**Flexibility and Control**

Control IP addressing (IPv4 or IPv6) and topology to create networks
that suit your workload—for example, create one network between web and
app servers, and another between app and database servers.

**High Availability**

Because multiple Cloud Servers can share the same IP address, you can
use fast IP address failover to enable high availability without making
a separate API call.

Customer benefits
^^^^^^^^^^^^^^^^^

+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Isolates your servers**         | Create Cloud Servers without Public or Private (ServiceNet) network interfaces, and make them accessible only through Cloud Networks.                                                                      |
+===================================+============================================================================================================================================================================================================+
| **Supports Clustering**           | Includes full support for broadcasting and multicasting required for some clustering technologies.                                                                                                         |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Simple Network Changes**        | Easily make networking changes to existing deployments without having to rebuild your Cloud Server.                                                                                                        |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **API Accessible**                | Use programmatic access to automatically create networks and attach/detach Cloud Servers based on workload requirements.                                                                                   |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Supports Complex Topologies**   | Combine with \ `Brocade Vyatta Routers <http://www.rackspace.com/cloud/servers/vrouter/>`__ to create complex topologies that route traffic between Cloud Networks or to external data centers over VPN.   |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **High Scalable**                 | Customers may have up to 10 Cloud Networks per region. Up to 250 Cloud Servers can be attached to a single Cloud network.                                                                                  |
+-----------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Pricing
^^^^^^^

FREE with every cloud account

Additional information
^^^^^^^^^^^^^^^^^^^^^^

-  open-source roots: `OpenStack
   Neutron <https://wiki.openstack.org/wiki/Neutron>`__

-  product overview: http://www.rackspace.com/cloud/networks

-  Cloud Networks: internal-use connections for Cloud Servers

Cloud Images at a glance
~~~~~~~~~~~~~~~~~~~~~~~~

★ core infrastructure: more in this guide at

 open-source roots: OpenStack Glance

 product overview: http://www.rackspace.com/cloud/images

$ PAY only for what you use

xxxxxxx

get details from

Cloud Block Storage at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

★ core infrastructure: more in this guide at

 open-source roots: OpenStack Cinder

 product overview: http://www.rackspace.com/cloud/block-storage

$ PAY only for what you use

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Block+Storage

Network services
----------------

Cloud DNS at a glance
~~~~~~~~~~~~~~~~~~~~~

 product overview: http://www.rackspace.com/cloud/dns

 FREE with every cloud account

xxxxxxx

get details from https://one.rackspace.com/display/productweb/Cloud+DNS

Cloud Load Balancers at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 product overview: http://www.rackspace.com/cloud/load-balancing

$ PAY only for what you use

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Load+Balancers

RackConnect at a glance
~~~~~~~~~~~~~~~~~~~~~~~

 product overview: http://www.rackspace.com/cloud/hybrid/rackconnect

$ PAY only for what you use

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/RackConnect+3

Storage & content delivery services
-----------------------------------

Cloud Backup at a glance
~~~~~~~~~~~~~~~~~~~~~~~~

 product overview: http://www.rackspace.com/cloud/backup

$ PAY only for what you use

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Backup

Cloud CDN at a glance
~~~~~~~~~~~~~~~~~~~~~

 product overview:
http://www.rackspace.com/cloud/cdn-content-delivery-network

$ PAY only for what you use

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Rackspace+CDN

Cloud Files at a glance
~~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: OpenStack Swift

 product overview: http://www.rackspace.com/cloud/files

$ PAY only for what you use

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Files

Data services
-------------

Cloud Big Data at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~

 product overview: http://www.rackspace.com/cloud/big-data

x

$ PAY only for what you use

Hadoop

xxxxxxx

get details from

Cloud Databases at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~~

 product overview: http://www.rackspace.com/cloud/databases

$ PAY only for what you use

MySQL, Percona Server, MariaDB

xxxxxxx

get details from

Object Rocket at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: Object Rocket

 product overview: http://objectrocket.com/

$ PAY only for what you use

MongoDB, Redis

xxxxxxx

get details from

Application services
--------------------

Auto Scale at a glance
~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: Otter

 product overview: http://www.rackspace.com/cloud/auto-scale

 FREE with every cloud account

xxxxxxx

get details from

Cloud Metrics at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~

 product overview:

xxxxxxx

get details from

Cloud Monitoring at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: Virgo

 product overview: http://www.rackspace.com/cloud/monitoring

 FREE with every cloud account

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Monitoring

Cloud Orchestration at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: OpenStack Heat

 product overview: http://www.rackspace.com/cloud/orchestration

 FREE with every cloud account

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Orchestration

Security & supporting services
------------------------------

Cloud Feeds at a glance
~~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: Atom Hopper

 product overview:

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Feeds

Cloud Identity at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~

 open-source roots: OpenStack Keystone

 product overview:

 FREE with every cloud account

xxxxxxx

get details from
https://one.rackspace.com/display/productweb/Cloud+Identity
