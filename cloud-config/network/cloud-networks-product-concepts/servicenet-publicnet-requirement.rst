.. _servicenet-publicnet-requirement:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Building servers without PublicNet or ServiceNet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
If a server is built without a PublicNet or ServiceNet network,
it cannot access certain Rackspace products and services.

However, it is possible to access some of these products (and
the Internet) indirectly via a
:ref:`Gateway Instance<network-gateway-instances>`.

In the diagram below, the web server and database server do not have
PublicNet attached. Instead, their outbound internet access is routed
through the Gateway Instance via Cloud Networks. The web server also has
public-facing services exposed via a Cloud Load Balancer, which connects
over ServiceNet.

.. figure:: /_images/gateway_instance_example.png
  :alt: Servers Behind a Gateway Instance

* PublicNet provides a server with direct access to the Internet.

* ServiceNet provides a server with access to Cloud Databases,
  Cloud Load Balancers, Cloud Files, Cloud Backup, Managed Cloud Support,
  and Windows activation. This network is required for all Managed Operations
  customers.

* Cloud Networks provides single-tenant, inter-server communication,
  and can provide indirect Internet access via a
  :ref:`Gateway Instance<network-gateway-instances>`.

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
How to Set Up Internet Access for Servers without PublicNet or ServiceNet
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

 For added security, you may opt to build servers without PublicNet or
 ServiceNet.

.. NOTE::
  The easiest way to do this is via
  `these Cloud Orchestration templates
  <https://github.com/rackerlabs/cloud-networks-orchestration.git>`_,
  which can create the Gateway Instance and a Cloud Network with all needed
  configuration at the same time.


1) Create a Cloud Network via the portal.
:rax-dev-docs:`Update the Cloud Network subnet
<cloud-networks/v2/api-reference/subnet-operations/#update-subnet>`
to include the following information:

  * **Gateway IP**: We recommend specifying the first available IP in your network
    range, such as '.1' for a /24 network.

  * **DNS Servers**: We recommend using the Rackspace DNS servers. Check the DNS
    configuration of your cloud servers to find the Rackspace DNS server IPs.
    Note that these will vary per region.

  * **Allocation Pool start and end**: This is the pool of IPs that will be assigned
    to any servers you build in the network. Do not include the gateway
    IP in this allocation pool, because you can't assign the gateway IP manually
    if it's in the allocation pool. To be safe, we recommend marking the 9th
    available IP as the start of the allocation pool. That will allow you to
    manually assign the first 8 IPs in the range as needed.

  * **(Optional) Host Routes**: Additional static routes that will be included
    in the routing table of any server connected to this subnet. Typically only
    needed when a VPN endpoint is a different host than the default gateway.

2)
:rax-dev-docs:`Create a fixed IP port
<cloud-networks/v2/api-reference/port-operations/#create-port>`
with the Gateway IP you specified in the previous
step.

3)
:rax-dev-docs:`Build a Gateway Instance
<cloud-servers/v2/api-reference/svr-basic-operations/#create-server>` with
PublicNet, and the fixed IP port you created in the previous step (ServiceNet
is optional.)

4) Configure NAT/routing on the Gateway Instance. Consult your OS distributor's
documentation as necessary.

5) To test routing, build a server with the Cloud Network attached, but
without PublicNet (ServiceNet is optional). Via the emergency console
or ServiceNet, login and verify that Internet access works. If it does not,
verify your previous steps.


.. include:: /_common/seealso-concepts-cloud-networks.txt
