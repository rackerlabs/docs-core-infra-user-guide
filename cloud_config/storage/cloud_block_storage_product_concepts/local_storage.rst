.. _local_storage:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Local storage for Cloud Servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Servers are generally created with a given amount of local storage
available to them in the form of one or more virtual hard disks. To best
utilize this local storage, you should understand the different types of
storage that are available.

Local storage technologies & terminology
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The virtual hard disks allocated to a Cloud Server are backed by one of
several different physical technologies, depending upon how you choose
to configure your Cloud Server. Each storage technology has specific
performance and cost characteristics.

Here is a high-level comparison of the technologies:

+-----------------------------------+-------------+-----------------------+----------------------+
| **Server Type**                   | **Speed**   | **Cost (relative)**   | **IOPS (maximum)**   |
+===================================+=============+=======================+======================+
| SATA (Standard Cloud Servers)     | Average     | Lowest                | ??                   |
+-----------------------------------+-------------+-----------------------+----------------------+
| SSD (Performance Cloud Servers)   | Fast        | Medium                | ??                   |
+-----------------------------------+-------------+-----------------------+----------------------+
| PCI (OnMetal)                     | Fastest     | Highest               | ??                   |
+-----------------------------------+-------------+-----------------------+----------------------+

Measuring local storage performance - IOPS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
There are many ways to capture the performance metrics of storage,
including 
Input/Output Operations per Second (IOPS). 
IOPS reports how many operations per second the
storage can handle. (An operation is typically a read or write of data.)

Several factors can cause the effective measured IOPS capability of
a storage medium to fluctuate, including system load, background
operations, or traffic from other virtual machines residing on the same
physical disks. Because of this, we list the IOPS capabilities of each
local storage option as the upper limit of its range, identifying 
the highest possible
IOPS that the device can process. This gives a picture of the
performance characteristics, but it is important to note that, as
mentioned, many factors can affect the IOPS rate during operation.

Local storage types associated with Cloud Server flavors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Choosing a flavor class for your Cloud Server also means choosing what
kind of local storage is available to that Cloud Server.

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

* the elasticity of cloud computing

* the consistent performance of colocated hosting

When you create a Cloud Server, if you make it an OnMetal Cloud Server,
you can choose one of three flavor classes designed to support specific
workloads:

* OnMetal I/O, optimized for databases

* OnMetal Memory, optimized for caching

* OnMetal Compute, optimized for CPU-intensive workloads

Every OnMetal flavor class provides 32GB for system disk. The OnMetal
I/O flavor class also provides Dual 1.6 TB PCIe flash cards for data
disk.

You can learn more about OnMetal at: 

* `OnMetal Cloud Servers <http://www.rackspace.com/cloud/servers/onmetal/>`__

* `OnMetal: The Right Way To Scale <http://www.rackspace.com/blog/onmetal-the-right-way-to-scale/>`__

* `What is new with OnMetal Cloud Servers <http://www.rackspace.com/knowledge_center/article/what-is-new-with-onmetal-cloud-servers>`__

* `Creating OnMetal Cloud Servers <http://www.rackspace.com/knowledge_center/article/creating-onmetal-cloud-servers>`__

Protecting local storage
^^^^^^^^^^^^^^^^^^^^^^^^
The virtual storage presented to your Cloud Server is backed by physical
hardware in RAID 10 configurations. RAID 10 means that multiple physical
disks in the same physical host would have to fail before there would be
a chance of data loss on your Cloud Server. Extensive hardware failure
of this nature is extremely unlikely, especially within the protective
environment of Rackspace data centers, but you may still be at risk for
data loss caused by human errors or human malice.

Rackspace **strongly recommends** that you use one or more of the
methods below to create and manage backup copies 
of your system and data
disks, providing an extra layer of protection and recoverability for
your Cloud Servers.

Backup method: snapshots
''''''''''''''''''''''''
Snapshots (also known as saved images or server images) can be
created using the API or Control Panel, and will save a complete copy of
your system disk. The image will be saved in your account and you will
be able to build a new Cloud Server from the image should the need
arise.

**Data disks are not captured when creating snapshots**. 
Only the system
disk is captured. 
You should use additional forms of backup if your data
disks hold critical data that must be protected.

Backup method: Cloud Backup
'''''''''''''''''''''''''''
Cloud Backup is a file-based backup application that lets you choose
which files and folders to backup from your Cloud Server. If you have
created a backup copy of your data, you can choose to restore all your
folders and files from the backup, or you can restore individual files
or folders from a given date, or restore to an entirely different Cloud
Server. For more about Cloud Backup, begin at
`Rackspace Cloud Backup - Overview <http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview>`__.

Backup method: Cloud Block Storage
''''''''''''''''''''''''''''''''''
You can use Cloud Block Storage to create and manage disk images that
are portable among your Cloud Servers. Cloud Block storage is part of
our core infrastructure; learn more about it at 
:ref:`cloud_block_storage_product_concepts`. 

Backup methods: custom
''''''''''''''''''''''
You can establish a custom backup process using a utility such as
`rsync <https://rsync.samba.org/>`__, an open-source utility that
provides fast incremental file transfer.

Storage-related offerings from Rackspace partners are listed in the
`Rackspace Marketplace <https://marketplace.rackspace.com/>`__. 
You may find one or more of these
that directly addresses your specific needs.
