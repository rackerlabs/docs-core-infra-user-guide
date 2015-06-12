.. _choose_flavor_class:

^^^^^^^^^^^^^^^^^^^^^^^
Choosing a flavor class
^^^^^^^^^^^^^^^^^^^^^^^
Flavor classes and flavors are often defined and grouped such that they
provide meaningful guidance in selecting the right choice for your
workload or application. The process of choosing the right flavor class
and flavor is generally analogous to choosing the resources and
specifications you would for physical hardware. Ultimately, choosing a
flavor class and flavor comes down to understanding your application
needs (both now and in the future), and balancing that against the
amount and type of resources it will need.

Some flavor classes are particularly well suited for specific workloads
such as web servers and database servers.

Web servers and other horizontally-scaling application tiers
''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
As web servers, such as Apache or Nginx, typically derive their
performance from network bandwidth, and to a lesser extent CPU and RAM,
versus disk space, choosing a **General Purpose** flavor can often be
the right decisions It has ample network bandwidth, and CPU and RAM
allocations that often match today’s highly optimized web server
applications.

Database servers
''''''''''''''''
These servers, whether SQL or NoSQL, often benefit from very fast disk,
and moderate to substantial amounts of RAM and CPU resources. While
these servers can be both vertically and horizontally scaled in
different scenarios, the application resources needed can often remain
significant. In these cases, an **I/O** flavor might be a good choice.

OnMetal servers
'''''''''''''''
**OnMetal**\ ™ flavors are ideal for a rapidly growing internet company.
OnMetal Cloud Servers are highly optimized for the following workloads:

* **OnMetal Compute**: high traffic web servers, application servers,
  load balancers, queue processing

* **OnMetal Memory**: large scale caches, index searches, in-memory
  analytics

* **OnMetal I/O**: large relational databases and noSQL data stores,
  Online Transaction Processing (OLTP) applications
