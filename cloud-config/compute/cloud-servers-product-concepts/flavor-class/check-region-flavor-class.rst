.. _check-region-flavor-class:

++++++++++++++++++++++++++++++++++++++++++++++++++++
Checking for regional availability of flavor classes
++++++++++++++++++++++++++++++++++++++++++++++++++++
Rackspace cloud servers are available to be created and consumed in
multiple regions. However, not all flavor classes and flavors may be
available in all regions. When planning a flavor class and flavor, be
sure to check the available flavors for the server's region.
You can get this information from
the :rax-dev:`Cloud Servers API <docs/cloud-servers/getting-started/>`
and the Cloud Control Panel.

If you use the
:mycloud:`Cloud Control Panel <>`
to create a cloud server,
you can choose its region from a pull-down list.
Other configuration options you can choose for that cloud server
through the Cloud Control Panel will then be
only those that are available in the selected region.

.. figure:: /_images/cloudservercreateregiondfw.png
   :alt: Choose a region for the server
         before choosing any other aspect of its configuration.

   *Choose a region for the server
   before choosing any other aspect of its configuration.*

Considerations other than the availability of a flavor class can
influence your choice of the optimal region
in which to create a new cloud server.
:kc-article:`About regions <about-regions>`
discusses some of the other factors
you should consider.
