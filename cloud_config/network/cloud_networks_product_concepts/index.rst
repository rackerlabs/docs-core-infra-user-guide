.. _cloud_networks_product_concepts:

============================
Understanding Cloud Networks
============================
Your Cloud Server configuration can include several kinds of networks,
connected as appropriate for your needs.

Typical use cases
~~~~~~~~~~~~~~~~~

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
~~~~~~~~~~~~~~~~~
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

Contents:

.. toctree::
   :maxdepth: 2

   network_cloud_servers
   network_onmetal_servers
   network_rackconnect
   publicnet
   servicenet
   DNS
