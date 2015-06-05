.. _cloud_servers_flavor_class:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Understanding flavor classes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A flavor class is a grouping of flavors based on similar
characteristics. Flavor classes streamline the process of choosing among
available resources or pricing models.

Flavor classes for virtual servers
''''''''''''''''''''''''''''''''''
To create your Cloud Server as a virtual server, open the Virtual Server
tab from the Cloud Control Panel.

.. figure:: /_images/CloudServerCreateVirtual.png
   :alt: Click the Virtual Server tab 
         to begin creating a virtual server.
   
   *Click the Virtual Server tab to begin creating a virtual server.*

You can choose Virtual Server flavor classes optimized for compute, I/O,
memory, general purpose, or standard resources:

* **Compute** is optimized for web servers, application servers and
  other CPU-intensive workloads. Storage is entirely backed by Cloud
  Block Storage, for maximum flexibility.

* **I/O** is optimized for applications demanding high disk I/O and
  consistent performance, such as large relational databases and
  NoSQL data stores. Storage is RAID 10-protected SSD.
  *Replaces Performance 2*.

* **Memory** is optimized for applications demanding low-latency access
  to large amounts of RAM, like caching servers, in-memory analytics
  and search indexes. Storage is entirely backed by Cloud Block
  Storage for maximum flexibility.

* **General Purpose** is great for web servers, batch processing,
  network appliances, small databases, and most general purpose
  computing workloads. Storage is high-performance, RAID 10-protected
  SSD.
  *Replaces Performance 1*.

* **Standard** scales resources like CPU, memory, and storage depending
  on your needs. All storage is located on RAID 10-protected SATA hard
  disk drives.

Flavor classes for OnMetal servers
''''''''''''''''''''''''''''''''''
To create your Cloud Server as an OnMetal™ server, open the OnMetal™
Server tab from the Cloud Control Panel.

.. figure:: /_images/CloudServerCreateOnMetal.png
   :alt: Click the OnMetal Server tab 
         to begin creating an OnMetal server.
   
   *Click the OnMetal Server tab to begin creating an OnMetal server.*

You can choose OnMetal™ Server flavor classes optimized for I/O, memory,
or compute resources:

-  **OnMetal I/O** is optimized for databases. OnMetal I/O servers are
   designed to support low-latency and extreme throughput to local
   storage, using a pair of the fastest PCIe flash cards that money can
   buy.

-  **OnMetal Memory** is optimized for caching. OnMetal Memory servers
   are designed for memory-intensive workloads such as Memcached or
   Redis. 512 GB servers and low-latency 10 Gb / s network enable modern
   architectures with the entire working set in RAM.

-  **OnMetal Compute** is optimized for web servers. OnMetal Compute
   servers are designed for connection handling and CPU-heavy workloads
   such as web serving. With high speeds, plenty of cores and a low-latency
   10 Gb/s network, OnMetal Compute is perfect for rendering
   web pages or pushing packets.

Contents:

.. toctree::
   :maxdepth: 2

   choose_flavor_class
   check_region_flavor_class
