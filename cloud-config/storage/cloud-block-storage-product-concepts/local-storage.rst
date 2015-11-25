.. _local-storage:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Local storage for cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud servers are generally created with a given amount of local storage
available to them in the form of one or more virtual hard disks. To best
use this local storage, you should understand the different types of
storage that are available.

Local storage technologies and terminology
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The virtual hard disks allocated to a cloud server are backed by one of
several different physical technologies, depending on how you choose
to configure the server. Each storage technology has specific
performance and cost characteristics.

Following is a high-level comparison of the technologies:

+-----------------------------------------------+-------------+-----------------------+
| **Server type**                               | **Speed**   | **Cost (relative)**   |
+===============================================+=============+=======================+
| SATA (Standard Cloud Servers)                 | Average     | Lowest                |
+-----------------------------------------------+-------------+-----------------------+
| SSD (I/O and General Purpose Cloud Servers)   | Fast        | Medium                |
+-----------------------------------------------+-------------+-----------------------+
| PCI (OnMetal)                                 | Fastest     | Highest               |
+-----------------------------------------------+-------------+-----------------------+

Measuring local storage performance: IOPS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
One way to compare the performance metrics of storage
is by using
Input/Output Operations per Second (IOPS).
IOPS reports the maximum number of operations per second the
storage can handle.
For the purpose of calculating IOPS,
an operation is typically a read or write of data.

Several factors can cause the effective measured IOPS capability of
a storage medium to fluctuate, including system load, background
operations, and traffic from other virtual machines residing on the same
physical disks. Because of this, consider any IOPS
measurements you obtain as describing the upper limit of each
local storage option's range, identifying
the highest possible
IOPS that the device can process. Although this provides information about
performance, it is important to remember that
many factors can affect the IOPS rate during operation. IOPS is most
useful as a basis of comparison
if you can control all other factors and run identical workloads
on systems that differ only in their storage configuration.

You can see the results of a performance experiment
comparing Rackspace storage technologies at
:rax-dev-blog:`Determining Optimal Storage based on IOPS <determining-optimal-storage-based-on-iops>`.
In that experiment,
Cloud Block Storage on SSD performed
better than any other option tested.
In a white paper on
:kc:`Cloud Block Storage (CBS) Benchmarking <whitepaper/cloud-block-storage-cbs-benchmarking>`,
performance quadrupled using Cloud Block Storage with SSD
as compared to Cloud Block Storage with SATA.

Local storage types associated with Cloud Servers flavors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Choosing a flavor class for your server also means choosing what
kind of local storage is available to that server.

* For Compute and Memory flavor classes, storage is entirely backed by
  Cloud Block Storage.

* For I/O and General Purpose flavor classes, storage is RAID 10 SSD.

* For Standard flavor classes, storage is RAID 10 SATA hard disk drives.

SATA local storage
''''''''''''''''''
Also known as spinning disk, Serial Advanced Technology Attachment
(SATA) disks are the traditional hard drives with physical platters
with which
most people are familiar. Because of efficiencies in engineering and
manufacturing over time, they can provide large capacities
at relatively
low prices. However, because of the physical spinning platters and moving
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
This speed comes at a literal cost because SSD
components are more expensive than SATA components.

Local storage types associated with OnMetal flavors
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
OnMetal Cloud Servers are backed by storage that complies with the
Peripheral Component Interconnect (PCI) local bus standard.

OnMetal Cloud Servers offer the benefits of the following
kinds of configuration:

* The elasticity of cloud computing

* The consistent performance of colocated hosting

When you create a server, if you make it an OnMetal server,
you can choose one of the following flavor classes designed to support specific
workloads:

* OnMetal I/O, optimized for databases

* OnMetal Memory, optimized for caching

* OnMetal Compute, optimized for CPU-intensive workloads

Every OnMetal flavor class provides 32 GB for the system disk. The OnMetal
I/O flavor class also provides Dual 1.6 TB PCIe flash cards for the data
disk.

For more information about OnMetal, see the following resources:

* :rax-cloud:`OnMetal Cloud Servers <servers/onmetal/>`

* :rax:`OnMetal: The Right Way To Scale <blog/onmetal-the-right-way-to-scale/>`

* :kc-article:`What is new with OnMetal Cloud Servers <what-is-new-with-onmetal-cloud-servers>`

* :kc-article:`Creating OnMetal Cloud Servers <creating-onmetal-cloud-servers>`

Protecting local storage
^^^^^^^^^^^^^^^^^^^^^^^^
The virtual storage presented to your cloud server is backed by physical
hardware in RAID 10 configurations. RAID 10 means that multiple physical
disks in the same physical host would have to fail before there would be
a chance of data loss on your server. Extensive hardware failure
of this nature is extremely unlikely, especially within the protective
environment of Rackspace data centers, but you might still be at risk for
data loss caused by human errors or human malice.

Rackspace **strongly recommends** that you use one or more of the
following methods to create and manage backup copies
of your system and data
disks, providing an extra layer of protection and recoverability for
your cloud servers.

Backup method: Snapshots
''''''''''''''''''''''''
You can create snapshots (also known as saved images or server images)
by using the API or Cloud Control Panel. Snapshots save a complete copy of
your system disk. The image is saved in your account and you can
build a new cloud server from the image.

**Data disks are not captured when you create snapshots**.
Only the system
disk is captured.
You should use additional forms of backup if your data
disks hold critical data that must be protected.

Backup method: Cloud Backup
'''''''''''''''''''''''''''
Cloud Backup is a file-based backup application that enables you
to choose
which files and folders to back up from your server. If you have
created a backup copy of your data, you can restore all your
folders and files from the backup, you can restore individual files
or folders from a given date, or you can restore to an entirely different
server. For more information about Cloud Backup, begin at
:kc-article:`Rackspace Cloud Backup - Overview <rackspace-cloud-backup-overview>`.

Backup method: Cloud Block Storage
''''''''''''''''''''''''''''''''''
You can use Cloud Block Storage to create and manage disk images that
are portable among your cloud servers. Cloud Block Storage is part of
our core infrastructure; learn more about it at
:ref:`cloud-block-storage-product-concepts`.

Backup methods: custom
''''''''''''''''''''''
You can establish a custom backup process by using a utility such as
`rsync <https://rsync.samba.org/>`__, an open-source utility that
provides fast incremental file transfer.

Storage-related offerings from Rackspace partners are listed in the
`Rackspace Marketplace <https://marketplace.rackspace.com/>`__.
You might find one or more of these
that directly addresses your specific needs.

.. include:: /_common/seealso-concepts-cloud-block-storage.txt
