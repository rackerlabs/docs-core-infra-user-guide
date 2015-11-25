.. _choose-flavor-class:

+++++++++++++++++++++++
Choosing a flavor class
+++++++++++++++++++++++
Flavor classes and flavors are often defined and grouped to help you
select the right choice for your
workload or application. The process of choosing the right flavor class
and flavor is generally analogous to choosing the resources and
specifications for physical hardware. Ultimately, choosing a
flavor class and flavor depends on understanding your application
needs (both now and in the future), and balancing those needs against the
necessary amount and type of resources.

Some flavor classes are particularly well suited for specific workloads
such as web servers and database servers.

Web servers and other horizontally scaling application tiers
''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
Because Web servers such as Apache and Nginx typically derive their
performance from network bandwidth, and to a lesser extent CPU and RAM,
choosing a **General Purpose** flavor can often be the right decision.
This flavor has ample network bandwidth, and CPU and RAM
allocations that are suited to highly optimized web server
applications.

Database servers
''''''''''''''''
Database servers, such as those running SQL or NoSQL,
often benefit from very fast disks
and moderate to substantial amounts of RAM and CPU resources. Although
these servers can be both vertically and horizontally scaled in
different scenarios, the application resources needed can often remain
significant. In these cases, an **I/O** flavor might be a good choice.

.. include:: /_common/seealso-concepts-cloud-servers.txt
