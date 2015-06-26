.. _check-region-flavor-class:

----------------------------------------------------
Checking for regional availability of flavor classes
----------------------------------------------------
Rackspace cloud servers are available to be created and consumed in
multiple regions. However, not all flavor classes and flavors may be
available in all regions. When planning a flavor class and flavor, be
sure to check the available flavors for the server's region.
You can get this information from 
the `Cloud Servers API <https://developer.rackspace.com/docs/cloud-servers/getting-started/>`__ 
and the Cloud Control Panel.

If you use the 
`Cloud Control Panel <https://mycloud.rackspace.com/>`__ 
to create a cloud server, 
you can choose its region from a pull-down list. 
Other configuration options you can choose for that cloud server
through the Cloud Control Panel will then be 
only those that are available in the selected region. 

.. figure:: /_images/CloudServerCreateRegionDFW.png
   :alt: Choose a region for the server 
         before choosing any other aspect of its configuration.
   
   *Choose a region for the server 
   before choosing any other aspect of its configuration.*

Considerations other than the availability of a flavor class can 
influence your choice of the optimal region 
in which to create a new cloud server. 
`About regions <http://www.rackspace.com/knowledge_center/article/about-regions>`__ 
discusses some of the other factors 
you should consider.