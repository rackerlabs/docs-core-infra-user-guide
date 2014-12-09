Software RAID
=============
.. example of expansion to compare hardware/software/hybrid RAID:
   http://www.adaptec.com/nr/rdonlyres/14b2fd84-f7a0-4ac5-a07a-214123ea3dd6/0/4423_sw_hwraid_10.pdf
   
A Redundant Array of Independent Disks (RAID)
array enables expansion of storage capacity by
combining many small disks rather than few large disks. 
RAID is 
generally not necessary for 
baseline performance and availability, 
but it may provide advantages in configurations 
that require extreme protection of in-flight data.

RAID can be implemented by hardware, software, or a hybrid of both. 
Software RAID uses a server's operating system to virtualize
and manage the RAID array. 
With Cloud Servers and Cloud Block Storage, 
you can create and use a
cloud-based software RAID array.

RAID arrays can be configured in several ways, 
each prioritizing different features.
RAID levels 0, 1, and 10 are widely used and are summarized
in the table below. 
Other RAID levels exist and may be appropriate
in specialized circumstances.

+----------------------+-----------------+-----------------------+-----------------------+
|Features              |RAID 0           |RAID 1                 |RAID 10                |
|                      |(striping)       |(mirroring)            |(mirroring +           |       
|                      |                 |                       |striping)              |
+======================+=================+=======================+=======================+
| Minimum drives       | 2               | 2                     | 4                     |
+----------------------+-----------------+-----------------------+-----------------------+
| Data protection      | High            | High                  | High                  |
+----------------------+-----------------+-----------------------+-----------------------+
| Read performance     | High            | High                  | High                  |
+----------------------+-----------------+-----------------------+-----------------------+
| Write performance    | High            | Medium                | Medium                |
+----------------------+-----------------+-----------------------+-----------------------+
| Read performance     | None            | Medium                | High                  |
| (degraded)           |                 |                       |                       |
+----------------------+-----------------+-----------------------+-----------------------+
| Write performance    | None            | High                  | High                  |
| (degraded)           |                 |                       |                       |
+----------------------+-----------------+-----------------------+-----------------------+
| Capacity utilization | 100%            | 50%                   | 50%                   |
+----------------------+-----------------+-----------------------+-----------------------+
| Typical applications | transitory data | transaction databases | application servers   |
+----------------------+-----------------+-----------------------+-----------------------+

Cloud Block Storage back-end storage volumes 
use RAID level 10.

Software RAID for Linux 
-----------------------
To learn how to set up software RAID on a cloud server running Linux, read 
http://www.rackspace.com/knowledge_center/article/configuring-a-software-raid-on-a-linux-general-purpose-cloud-server.

Software RAID for Windows
-------------------------

* Windows Server 2012 named its RAID capability "Storage Spaces".
  You can read about Storage Spaces at http://technet.microsoft.com/en-us/library/hh831739.aspx.
* Windows Server 2008 provides two ways to interact with RAID
  devices:

    * GUI via Diskmgmt.msc 
    * CLI via Diskpart.exe
  
  You can read about both at 
  http://msdn.microsoft.com/en-us/library/dd163558.aspx.
