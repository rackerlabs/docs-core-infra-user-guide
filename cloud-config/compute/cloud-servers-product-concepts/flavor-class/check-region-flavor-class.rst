.. _check-region-flavor-class:

++++++++++++++++++++++++++++++++++++++++++++++++++++
Checking for regional availability of flavor classes
++++++++++++++++++++++++++++++++++++++++++++++++++++
Rackspace cloud servers can be created and consumed in
multiple regions. However, not all flavor classes and flavors are
available in all regions. When planning a flavor class and flavor, be
sure to check the available flavors for the server's region.
You can get this information from
the :rax-dev-quickstart:`Cloud Servers API <cloud-servers/getting-started/>`
and the Cloud Control Panel.

If you use the
:mycloud:`Cloud Control Panel <>`
to create a cloud server,
you can choose its region from a pull-down list. Selecting a region
during server creation then limits other configuration options to
only those that are available in the selected region.
Other configuration options you can choose for that cloud server

.. figure:: /_images/cloudservercreateregiondfw.png
   :alt: Choose a region for the server
         before choosing any other aspect of its configuration.

   *Choose a region for the server
   before choosing any other aspect of its configuration.*

Considerations other than the availability of a flavor class can
influence your choice of the optimal region
in which to create a new cloud server.
:how-to:`About regions <about-regions>`
discusses some of the other factors
you should consider.

.. include:: /_common/seealso-concepts-cloud-servers.txt
