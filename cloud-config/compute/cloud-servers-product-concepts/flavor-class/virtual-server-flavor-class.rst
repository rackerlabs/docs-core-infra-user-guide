.. _virtual-server-flavor-class:

++++++++++++++++++++++++++++++++++++++++
Flavor classes for virtual cloud servers
++++++++++++++++++++++++++++++++++++++++
To create your server as a virtual server, open the **Virtual Server**
tab on the Create Server page of the Cloud Control Panel.

.. figure:: /_images/cloudservercreatevirtual.png
   :alt: Click the Virtual Server tab
         to begin creating a virtual server.

   *Click the Virtual Server tab to begin creating a virtual server.*

You can choose Virtual Server flavor classes optimized for compute, I/O,
memory, general purpose, or standard resources:

* **Compute** is optimized for web servers, application servers and
  other CPU-intensive workloads. Storage is entirely backed by Cloud
  Block Storage, for maximum flexibility.

* **I/O** is optimized for applications that demand high disk I/O and
  consistent performance, such as large relational databases and
  NoSQL data stores. Storage is RAID 10-protected SSD.

* **Memory** is optimized for applications that demand low-latency access
  to large amounts of RAM, like caching servers, in-memory analytics
  and search indexes. Storage is entirely backed by Cloud Block
  Storage for maximum flexibility.

* **General Purpose** is for web servers, batch processing,
  network appliances, small databases, and most general purpose
  computing workloads. Storage is high-performance, RAID 10-protected
  SSD.

* **Standard** scales resources like CPU, memory, and storage depending
  on your needs. All storage is located on RAID 10-protected SATA hard
  disk drives.

.. include:: /_common/seealso-concepts-cloud-servers.txt
