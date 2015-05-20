.. _tour_network_services:

----------------
Network services
----------------
Services in this category include

* Cloud Networks 
* Cloud DNS
* Cloud Load Balancers
* RackConnect

.. NOTE::
   **Cloud Networks** is part of the 
   core infrastructure of the Rackspace cloud, 
   the focus of this guide. 
   
   A good place to begin learning to interact with it is
   :ref:`cloud_interfaces`. 

Cloud Networks at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~
* product overview at 
  http://www.rackspace.com/cloud/networks

* FREE with every cloud account

* open-source roots: 
  `OpenStack Neutron <https://wiki.openstack.org/wiki/Neutron>`__

Cloud Networks enables customers to create and manage secure, isolated
networks in the cloud. 
These networks are fully single tenant, and
customers have complete control over the network topology, 
IP addressing (IPv4 or IPv6), 
and which Cloud Servers are connected to the network.

Typical use cases
^^^^^^^^^^^^^^^^^

**Security**

  Get fully isolated, single-tenant Layer 2 networks designed to securely
  transfer sensitive information between Cloud Servers located in the same
  region.

**Flexibility and control**

  Control IP addressing (IPv4 or IPv6) and topology to create networks
  that suit your workload—for example, create one network between web and
  app servers, and another between app and database servers.

**High availability**

  Because multiple Cloud Servers can share the same IP address, you can
  use fast IP address failover to enable high availability without making
  a separate API call.

Customer benefits
^^^^^^^^^^^^^^^^^
These are some of the ways in which Cloud Networks can 
be useful within your Cloud Servers configuration: 

* **Isolate your servers**

  You can create Cloud Servers without public or 
  private (ServiceNet) network interfaces, 
  making them accessible only through Cloud Networks.

* **Support clustering** 

  Includes full support for broadcasting and multicasting as 
  required for some clustering technologies.

* **Simplify network changes**

  You can make networking changes to existing deployments 
  without having to rebuild your Cloud Server.

* **Automate network changes**

  Via the Cloud Networks API, 
  you can develop custom software to automatically 
  create networks and attach or detach Cloud Servers 
  based on workload requirements.

* **Support complex topologies**

  Combine with 
  `Brocade Vyatta Routers <http://www.rackspace.com/cloud/servers/vrouter/>`__ 
  to create complex topologies that route traffic 
  between Cloud Networks or to external data centers over VPN.

* **Scale networks as you grow** 

  Up to 250 Cloud Servers can be attached to a single cloud network.
  You can have up to 10 cloud networks per region. 

Cloud DNS at a glance
~~~~~~~~~~~~~~~~~~~~~
* product overview at  
  http://www.rackspace.com/cloud/dns

* FREE with every cloud account

Cloud Load Balancers at a glance
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* product overview at  
  http://www.rackspace.com/cloud/load-balancing

* `PAY only for what you use <http://www.rackspace.com/cloud/public-pricing>`__

RackConnect at a glance
~~~~~~~~~~~~~~~~~~~~~~~
* product overview at  
  http://www.rackspace.com/cloud/hybrid/rackconnect

* `PAY only for what you use <http://www.rackspace.com/cloud/public-pricing>`__

