Software RAID
=============

[TODO: expand text]
    Generally not necessary for baseline performance and availability
    General description of common RAID options and why
        RAID 0 - larger volumes and more RW IOPS
        RAID 1 - more protection, ½ space, more R IOPS
        RAID 10 - more RW IOPS, protection, 1/2 space


RAID for Linux 
--------------
To learn how to set up software RAID on a cloud server running Linux, read 
http://www.rackspace.com/knowledge_center/article/configuring-a-software-raid-on-a-linux-general-purpose-cloud-server.

RAID for Windows
----------------

* Windows Server 2012 named its RAID capability "Storage Spaces".
` You can read about Storage Spaces at http://technet.microsoft.com/en-us/library/hh831739.aspx.
* Windows Server 2008 provides two ways to interact with RAID
``devices:

    * GUI via Diskmgmt.msc 
    * CLI via Diskpart.exe
  
  You can read about both at 
  http://msdn.microsoft.com/en-us/library/dd163558.aspx.
