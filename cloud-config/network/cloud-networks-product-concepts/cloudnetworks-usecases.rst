.. _cloudnetworks-usecases:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Typical use cases for Cloud Networks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Networks is especially useful for
tightening security, increasing flexibility,
and maintaining uninterrupted availability.

**Secure east and west traffic**

  Get fully isolated, single-tenant Layer 2 networks designed to securely
  transfer sensitive information between servers located in the same
  region.

**Enforce consistent network configuration**

 Program static routes, the gateway IP, and DNS servers into the Cloud Network API
 and have them automatically injected in your servers at boot time
 or when the network is attached.
 Use a :ref:`Gateway Instances<network-gateway-instances>` to connect your
 isolated Cloud Servers to the Internet.

**VPN endpoint**

  Securely connect to remote resources via VPN. By programming static routes
  into your Cloud Networks subnet, you can ensure that all servers attached
  to your Cloud Network can access the remote networks connected via VPN.

**High availability**

  Because multiple servers can share the same IP address, you can
  use fast IP address failover to enable high availability without making
  a separate API call.

.. include:: /_common/seealso-concepts-cloud-networks.txt
