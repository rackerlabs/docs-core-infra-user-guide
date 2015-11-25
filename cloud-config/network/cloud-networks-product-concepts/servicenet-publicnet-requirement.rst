.. _servicenet-publicnet-requirement:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
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

.. include:: /_common/seealso-concepts-cloud-networks.txt
