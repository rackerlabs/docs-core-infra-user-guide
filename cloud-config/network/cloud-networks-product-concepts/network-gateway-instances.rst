.. _network-gateway-instances:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Gateway Instances in Rackspace Cloud
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A Gateway Instance is a Rackspace Cloud Server that routes traffic between the
public internet and any other Rackspace Cloud Servers that do not have a public
IP. A Gateway Instance is typically a virtual network appliance, but could
also be a Linux or Windows server.

In the diagram below, the web server and database server do not have
PublicNet attached. Instead, their outbound internet access is routed
through the Gateway Instance by using Cloud Networks. The web server also has
public-facing services exposed by using a Cloud Load Balancer, which connects
over ServiceNet.

.. figure:: /_images/gateway_instance_example.png
  :alt: Servers Behind a Gateway Instance

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Creating a Gateway Instance in Rackspace Cloud by using Orchestration (recommended)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The easiest way to create a Gateway Instance is by using
:rackerlabs:`these Cloud Orchestration templates
<cloud-networks-orchestration>`
that create the Gateway Instance and a Cloud Network with
all needed configuration (the gateway IP and DNS Servers) at the same time.

To use the Cloud Orchestration template, copy the template to your clipboard,
then navigate to the :mycloud:`Cloud Control Panel <>` and click
**Orchestration**,
then click **Stack Templates**. From that page, click **Create Custom Template**.
Paste the template into the text box, then click **Create Template and Launch
Stack**.

Fill in the stack details with your preferred information, such as administrative
password, preferred IP scheme, and so on.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Creating a Gateway Instance in Rackspace Cloud manually
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you wish to create the Gateway Instance manually, see the section entitled
"How to set up Internet access for servers without PublicNet or ServiceNet"
within the :ref:`Building servers without PublicNet or ServiceNet
<servicenet-publicnet-requirement>` section of this guide.
