.. _software-raid:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Software RAID for Cloud Block Storage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A redundant array of independent disks (RAID) enables expansion of
storage capacity by combining many small disks rather than a few large
disks. RAID is generally not necessary for baseline performance and
availability, but it might provide advantages in configurations that
require extreme protection of in-flight data.

RAID can be implemented by hardware, software, or a hybrid of both.
Software RAID uses a server's operating system to virtualize and manage
the RAID array. With Cloud Servers and Cloud Block Storage, you can
create and use a cloud-based software RAID array.

RAID arrays can be configured in several ways, each prioritizing
different features. RAID levels 0, 1, and 10 are widely used and are
summarized in the following table. Other RAID levels exist and might be
appropriate in specialized circumstances. Cloud Block Storage
back-end storage volumes use RAID level 10.

+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| **Features**                   | **RAID 0 (striping)**   | **RAID 1 (mirroring)**   | **RAID 10 (mirroring + striping)**   |
+================================+=========================+==========================+======================================+
| Minimum drives                 | 2                       | 2                        | 4                                    |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Data protection                | High                    | High                     | High                                 |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Read performance               | High                    | High                     | High                                 |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Write performance              | High                    | Medium                   | Medium                               |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Read performance (degraded)    | None                    | Medium                   | High                                 |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Write performance (degraded)   | None                    | High                     | High                                 |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Capacity utilization           | 100%                    | 50%                      | 50%                                  |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+
| Typical applications           | Transitory data         | Transaction databases    | Application servers                  |
+--------------------------------+-------------------------+--------------------------+--------------------------------------+

Software RAID for Linux
'''''''''''''''''''''''
To learn how to set up software RAID on a cloud server running Linux,
read
:how-to:`Configuring a Software RAID on a Linux General Purpose Cloud Server <configuring-a-software-raid-on-a-linux-general-purpose-cloud-server>`.

Software RAID for Windows
'''''''''''''''''''''''''
Windows tools for RAID have different names in different versions of
Windows.

Windows Server 2012 named its RAID capability *Storage Spaces*. You can
read about Storage Spaces
in Microsoft's
`Storage Spaces Overview <http://technet.microsoft.com/en-us/library/hh831739.aspx>`__.

Windows Server 2008 provides the following ways to interact with RAID devices:

* GUI via ``Diskmgmt.msc``

* CLI via ``Diskpart.exe``

You can read about both Diskmgmt and Diskpart
in Microsoft's
`Overview of Disk Management <http://msdn.microsoft.com/en-us/library/dd163558.aspx>`__.

.. include:: /_common/seealso-concepts-cloud-block-storage.txt
