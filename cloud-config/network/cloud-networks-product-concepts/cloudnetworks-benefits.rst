.. _cloudnetworks-benefits:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Customer benefits from Cloud Networks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
These are some of the ways in which Cloud Networks can
be useful within your Cloud Servers configuration:

* **Isolate your servers**

    You can create servers without public or
    private (ServiceNet) network interfaces,
    making them accessible only through Cloud Networks.

* **Full control over IP addresses**

  Unlike PublicNet and ServiceNet, it is possible to assign
  specific Cloud Networks IPs to Cloud Servers, either at build time
  (by creating a port with a fixed IP) or to an existing server (by creating
  a port with a fixed IP and the existing server's UUID as device ID).

* **Enforce consistent network configuration**

  Program routes, the gateway IP, and DNS servers into the Cloud Network API
  and have them automatically injected in your servers at build time
  or when the network is attached.
  Use a :ref:`Gateway Instance<network-gateway-instances>` to connect your
  isolated Cloud Servers to the Internet.

* **NAT or VPN endpoint or network segmentation**

    Combine Cloud Networks with
    :ref:`Gateway Instances<network-gateway-instances>`
    to connect your isolated Cloud Servers to the Internet.
    You can also use Cloud Networks to connect your isolated
    Cloud Servers to a VPN endpoint, enabling secure connectivity
    to resources outside Rackspace Cloud. Within Rackspace Cloud, you can
    also use multiple Cloud Networks to segment traffic.

* **Cluster your applications**

    Cloud Networks includes full support
    for broadcasting and multicasting as
    required for some clustering technologies.

* **Simplify network changes**

    You can make networking changes to existing deployments
    without having to rebuild your server.

* **Automate network changes**

    By using the Cloud Networks API or Cloud Orchestration,
    you can develop custom software to automatically
    create networks and attach or detach servers
    based on workload requirements.


* **Scale networks as you grow**

    You can attach up to 250 servers to a single cloud network.
    You can have up to 10 cloud networks per region.

.. include:: /_common/seealso-concepts-cloud-networks.txt
