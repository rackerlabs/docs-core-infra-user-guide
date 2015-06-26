.. _choose-flavor-class:

-----------------------
Choosing a flavor class
-----------------------
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
Web servers such as Apache and Nginx typically derive their
performance from network bandwidth, and to a lesser extent CPU and RAM; 
disk performance is probably not a major factor in 
the performance of such a server. 
A **General Purpose** flavor can often be
the right choice for a web server. 
These flavors provide ample network bandwidth and their CPU and RAM
allocations are suited to highly optimized web server
applications.

Database servers
''''''''''''''''
Database servers, such as those running SQL or NoSQL, 
often benefit from very fast disk 
and moderate to substantial amounts of RAM and CPU resources. While
these servers can be both vertically and horizontally scaled in
different scenarios, the application resources needed can often remain
significant. In these cases, an **I/O** flavor might be a good choice.
