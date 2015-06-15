.. _local-storage:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Local storage for cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud servers are generally created with a given amount of local storage
available to them in the form of one or more virtual hard disks. To best
utilize this local storage, you should understand the different types of
storage that are available.

Local storage technologies & terminology
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The virtual hard disks allocated to a cloud server are backed by one of
several different physical technologies, depending upon how you choose
to configure your server. Each storage technology has specific
performance and cost characteristics.

Here is a high-level comparison of the technologies:

+-----------------------------------+-------------+-----------------------+
| **Server type**                   | **Speed**   | **Cost (relative)**   |
+===================================+=============+=======================+
| SATA (Standard Cloud Servers)     | Average     | Lowest                |
+-----------------------------------+-------------+-----------------------+
| SSD (Performance Cloud Servers)   | Fast        | Medium                |
+-----------------------------------+-------------+-----------------------+
| PCI (OnMetal)                     | Fastest     | Highest               |
+-----------------------------------+-------------+-----------------------+

Measuring local storage performance - IOPS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
One way to compare the performance metrics of storage 
is by observing  
Input/Output Operations per Second (IOPS). 
IOPS reports the maximum number of operations per second the
storage can handle. 
For the purpose of calculating IOPS, 
an operation is typically a read or write of data.

Several factors can cause the effective measured IOPS capability of
a storage medium to fluctuate, including system load, background
operations, or traffic from other virtual machines residing on the same
physical disks. Because of this, consider any IOPS 
measurements you obtain as describing the upper limit of each
local storage option's range, identifying 
the highest possible
IOPS that the device can process. This gives a picture of the
performance characteristics, but it is important to remember that 
many factors can affect the IOPS rate during operation. IOPS is most 
useful as a basis of comparison 
if you can control all other factors and run identical workloads 
on systems that differ only in their storage configuration.

You can see the results of a performance experiment  
comparing Rackspace storage technologies at 
`Determining Optimal Storage based on IOPS <https://developer.rackspace.com/blog/determining-optimal-storage-based-on-iops/>`__. 
In that experiment, 
Cloud Block Storage on SSD performed 
better than any other option tested.
In a white paper on 
`Cloud Block Storage (CBS) Benchmarking <http://www.rackspace.com/knowledge_center/whitepaper/cloud-block-storage-cbs-benchmarking>`__,
performance quadrupled using Cloud Block Storage with SSD 
as compared to Cloud Block Storage with SATA. 

Local storage types associated with Cloud Servers flavors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Choosing a flavor class for your server also means choosing what
kind of local storage is available to that server.

* In Compute and Memory flavor classes, storage is entirely backed by
   Cloud Block Storage.

* In I/O and General Purpose flavor classes, storage is RAID 10 SSD.

* In Standard flavor classes, storage is RAID 10 SATA hard disk drives.

SATA local storage
''''''''''''''''''
Also known as spinning disk, Serial Advanced Technology Attachment
(SATA) are the traditional hard drives with physical platters 
with which
most people are familiar. Due to efficiencies in engineering and
manufacturing over time, they can provide large capacities 
at relatively
low prices. However, due to the physical spinning platters and moving
write heads of SATA disks, they are slower than newer technologies 
such as 
SSD in many situations.

SSD local storage
'''''''''''''''''
Solid State Disk (SSD) 
uses persistent RAM technology to store data.
Because SSD 
has no moving parts, locating and reading any given bit of data from the
disk is extremely fast
when compared to SATA, which is delayed by the 
movements of platters and write heads. 
This speed comes at a cost, literally, as SSD
components are more expensive and thus are priced higher relative to
SATA components.

Local storage types associated with OnMetal flavors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
OnMetal Cloud Servers are backed by storage that complies with the
Peripheral Component Interconnect (PCI) local bus standard.

OnMetal Cloud Servers offer the benefits of two kinds of configuration:

* The elasticity of cloud computing

* The consistent performance of colocated hosting

When you create a server, if you make it an OnMetal server,
you can choose one of three flavor classes designed to support specific
workloads:

* OnMetal I/O, optimized for databases

* OnMetal Memory, optimized for caching

* OnMetal Compute, optimized for CPU-intensive workloads

Every OnMetal flavor class provides 32 GB for the system disk. The OnMetal
I/O flavor class also provides Dual 1.6 TB PCIe flash cards for data
disk.

You can learn more about OnMetal at: 

* `OnMetal Cloud Servers <http://www.rackspace.com/cloud/servers/onmetal/>`__

* `OnMetal: The Right Way To Scale <http://www.rackspace.com/blog/onmetal-the-right-way-to-scale/>`__

* `What is new with OnMetal Cloud Servers <http://www.rackspace.com/knowledge_center/article/what-is-new-with-onmetal-cloud-servers>`__

* `Creating OnMetal Cloud Servers <http://www.rackspace.com/knowledge_center/article/creating-onmetal-cloud-servers>`__

Protecting local storage
^^^^^^^^^^^^^^^^^^^^^^^^
The virtual storage presented to your cloud server is backed by physical
hardware in RAID 10 configurations. RAID 10 means that multiple physical
disks in the same physical host would have to fail before there would be
a chance of data loss on your server. Extensive hardware failure
of this nature is extremely unlikely, especially within the protective
environment of Rackspace data centers, but you may still be at risk for
data loss caused by human errors or human malice.

Rackspace **strongly recommends** that you use one or more of the
methods below to create and manage backup copies 
of your system and data
disks, providing an extra layer of protection and recoverability for
your cloud servers.

Backup method: Snapshots
''''''''''''''''''''''''
Snapshots (also known as saved images or server images) can be
created using the API or Cloud Control Panel, and will save a complete copy of
your system disk. The image will be saved in your account and you will
be able to build a new cloud server from the image should the need
arise.

**Data disks are not captured when creating snapshots**. 
Only the system
disk is captured. 
You should use additional forms of backup if your data
disks hold critical data that must be protected.

Backup method: Cloud Backup
'''''''''''''''''''''''''''
Cloud Backup is a file-based backup application that lets you choose
which files and folders to backup from your server. If you have
created a backup copy of your data, you can choose to restore all your
folders and files from the backup, or you can restore individual files
or folders from a given date, or restore to an entirely different
server. For more about Cloud Backup, begin at
`Rackspace Cloud Backup - Overview <http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview>`__.

Backup method: Cloud Block Storage
''''''''''''''''''''''''''''''''''
You can use Cloud Block Storage to create and manage disk images that
are portable among your cloud servers. Cloud Block Storage is part of
our core infrastructure; learn more about it at 
:ref:`cloud-block-storage-product-concepts`. 

Backup methods: Custom
''''''''''''''''''''''
You can establish a custom backup process using a utility such as
`rsync <https://rsync.samba.org/>`__, an open-source utility that
provides fast incremental file transfer.

Storage-related offerings from Rackspace partners are listed in the
`Rackspace Marketplace <https://marketplace.rackspace.com/>`__. 
You may find one or more of these
that directly addresses your specific needs.
