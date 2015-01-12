Cloud Server Local Storage 
==========================
Cloud Servers are generally created with a given amount of local storage
available to them in the form of one or more virtual hard disks.  In order to
best utilize this local storage, the user needs to understand the different
types and characteristics that are available.

Local storage technologies & terminology
----------------------------------------- 
The virtual hard disks allocated to
a Cloud Server are backed by one of several 
different physical technologies, 
depending upon how you choose to configure your Cloud Server.
Each storage technology has 
specific performance and cost characteristics. 

Here is a high-level comparison of the technologies:

+---------------------------------+---------+------------+-----------+
| Server Type                     | Speed   | Cost       | IOPS      |
|                                 |         | (relative) | (maximum) |
+=================================+=========+============+===========+
| SATA (Standard Cloud Servers)   | Average | Lowest     | ??        |
+---------------------------------+---------+------------+-----------+
| SSD (Performance Cloud Servers) | Fast    | Medium     | ??        |
+---------------------------------+---------+------------+-----------+
| PCI (OnMetal)                   | Fastest | Highest    | ??        |
+---------------------------------+---------+------------+-----------+ 

Measuring local storage performance - IOPS
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ 
There are many ways to capture the performance metrics of storage, including
the common measurment "IOPS". IOPS
stands for Input/Output Operations per Second, and captures how many operations
per second the storage can handle. (An operation is typically a read or write
of data.)

A number of factors can cause the effective measured IOPS capability of a
storage medium to fluctuate, including system load, background operations, or
traffic from other virtual machines residing on the same physical disks.
Because of this, we list the IOPS capabilities of each local storage option as
an "up-to" number: i.e. the highest possible IOPS that the device can process.
This gives a picture of the performance characteristics, but it is important to
note that, as mentioned, many factors can affect the IOPS rate during
operation. 

Cloud Server flavors and local storage types
--------------------------------------------
Choosing a flavor class for your Cloud Server  
also means choosing what kind of local storage 
is available to that Cloud Server.

* in Compute and Memory flavor classes, storage is entirely backed by Cloud Block Storage.
* in I/O and General Purpose flavor classes, storage is RAID 10-protected SSD.
* in Standard flavor classes, storage is RAID 10-protected SATA hard disk drives

SATA local storage
^^^^^^^^^^^^^^^^^^ 
Also known as "spinning
disk", Serial Advanced Technology Attachment (SATA) 
are the traditional hard drives with physical platters with which
most people are familiar. Due to efficiencies in engineering and manufacturing
over time, they can provide large capacities at relatively low prices. However,
due to the physical spinning platters and moving write heads of SATA disks,
they are slower than newer technologies like SSD in many situations. 

SSD local storage
^^^^^^^^^^^^^^^^^
SSD stands for Solid State Disk. Instead of the platters and write heads
of SATA, SSD uses persistant RAM technology to store data. 
Because SSD has no moving parts, locating
and reading any given bit of data from the disk is extremely fast. 
This speed comes at a cost, literally, as SSD components
are more expensive and thus are priced higher relative to SATA/spinning disks.

OnMetal flavors and local storage types
---------------------------------------
OnMetal Cloud Servers are backed by storage 
that complies with the 
Peripheral Component Interconnect (PCI) local bus standard.

OnMetal Cloud Servers offer the benefits 
of two kinds of configuration:

* the elasticity of cloud computing
* the consistent performance of colocated hosting 

When you create a Cloud Server, 
if you make it an OnMetal Cloud Server, 
you can choose one of three flavor classes 
designed to support specific workloads:

* OnMetal I/O, optimized for databases
* OnMetal Memory, optimized for caching
* OnMetal Compute, optimized for CPU-intensive workloads

Every OnMetal flavor class provides 
32GB for system disk. 
The OnMetal I/O flavor class also 
provides 
Dual 1.6 TB PCIe flash cards
for data disk.

You can learn more about OnMetal in the Cloud Control Panel and at 

* http://www.rackspace.com/cloud/servers/onmetal/ 
* http://www.rackspace.com/blog/onmetal-the-right-way-to-scale/
* http://www.rackspace.com/knowledge_center/article/what-is-new-with-onmetal-cloud-servers
* http://www.rackspace.com/knowledge_center/article/creating-onmetal-cloud-servers 

System and data disks 
---------------------
Different flavors of Cloud Servers are given different allocations of system
and data disks. 

**Standard / General Cloud Servers**: 1 System Disk **Performance Cloud
Servers**: 1 System Disk, 1 or more Data Disks

(we can put a table in here if we want but it'll be a bit of a hassle and might
get outdated...link to RS.com?)

System Disk 
^^^^^^^^^^^
The system disk, also called "boot disk", is the first disk
the server will attempt to access and boot from, much like the first physical
hard drive plugged into a physical computer. Operating systems are installed
on this disk by default. Data can be stored on a system disk,
although it may have less capacity than any attached data disks. 

.. NOTE::
   To make a back up copy of a *system* disk, 
   use Cloud Images to create a bootable backup.

Data Disks 
^^^^^^^^^^
Data disk space is in addition to the system disk. 
Some Cloud Server flavors to not have data disks assigned to them.
If your Cloud Server has a data disk, is is available to use for your
application data, caching, or other purposes.

Data disks are provided as
empty or raw disks in some cases, 
to allow you maximum flexibility in how you
use them. 
Before you can use a data disk, 
you may need to format it, partition it, 
or group it into a
software RAID group. 

To prepare a data disk for use on a Cloud Server, 
follow the steps appropriate for 
that Cloud Server's 
the operating system:

* for Linux, see http://www.rackspace.com/knowledge_center/article/preparing-data-disks-on-linux-cloud-servers.
* for Windows, see http://www.rackspace.com/knowledge_center/article/preparing-data-disks-on-windows-cloud-servers. 

.. NOTE::
   To make a back up copy of a *data* disk, use:
    
   * Cloud Backup for incremental backups, such as for disaster recovery
   * Cloud Block Storage for portability, such as for creation of new servers

Protecting local storage 
------------------------ 
The virtual storage presented to your Cloud Server is backed by physical
hardware in RAID10 configurations.  RAID10 means that multiple physical disks
in the same physical host would have to fail before there would be a chance of
data loss on your Cloud Server. 

However, it is **strongly recommended** that you use one or more of the
available methods below to provide an extra layer of protection for your System
and/or Data Disks.

Snapshots 
^^^^^^^^^ 
Snapshots (also known as "saved images" or "server images")
can be created using the API or Control Panel, and will save a complete copy of
your System Disk. The image will be saved in your account and you will be able
to build a new Cloud Server from the image should the need arise. 

It has been mentioned, but is very critical so bears repeating: **Data Disks
are not captured when creating snapshots**! Only the System disk is captured.
You should use additional forms of backup if your Data Disks hold critical data
that needs to be protected.

Cloud Backup 
^^^^^^^^^^^^ 
I'll come back to this XXXXX

Cloud Block Storage 
^^^^^^^^^^^^^^^^^^^ 
I'll come back to this XXXXXXX

Custom methods 
^^^^^^^^^^^^^^ 
Rsync, etc. Not sure how far to go down this path 

(below was lifted from KC article, not sure what to do with it yet)

Performance servers use faster solid state drives (SSD) and separate the system
disk from the data disk, with both disks equally RAID 10 protected. With your
operating system on a separate disk from your data, you can more easily create
an image of the system disk because it is a fixed size and doesn't scale up as
other resources increase. For more information on data disk imaging
limitations, see Images Capture System Disk Only (below) or for the full
procedure,see Creating an Image of Your Performance Cloud Server with the
Control Panel. You can back up the data on your data disk or disks by
leveraging either Rackspace Cloud Backup or Rackspace Cloud Block Storage (an
option that can also be used to increase the storage capacity of your server,
if needed). For a comparison of the two data disk backup options, see Best
Practices for Backing Up Your Data: Cloud Block Storage versus Cloud Backup.

