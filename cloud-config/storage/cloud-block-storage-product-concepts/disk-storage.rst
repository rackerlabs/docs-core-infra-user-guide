.. _disk-storage:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
System and data disks for cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Different flavors of cloud servers are allocated different sizes and
numbers of system and data disks.

To see what disk configuration is associated with each flavor, use the
Cloud Control Panel to display the options available to you when you
create a server.

For example, compare the disk configuration offered for a server
with 60 GB of RAM in two different flavor classes:

* In the I/O flavor class, the configuration for this server
  includes a 40-GB system disk and 600-GB data disk
  (addressable as two disks).

* In the Compute flavor class, the configuration for this
  server includes a 50-GB system disk and no data disk.

System disk
^^^^^^^^^^^
The *system disk*, also called the *boot disk*, is the first disk
from which the server
will attempt to access and boot,
much like the first physical hard
drive plugged into a physical computer.
Operating systems are installed
on this disk by default.
Data can be stored on a system disk, although
it might have less capacity than any attached data disks.

.. TIP::
   To make a backup copy of a *system* disk,
   use Cloud Images to create a
   bootable backup.

Data disks
^^^^^^^^^^
Data disk space is in addition to the system disk. Some Cloud Servers
flavors do not have data disks assigned to them. If your server
has a data disk, it is available to use for your application data,
caching, or other purposes.

Data disks are provided as empty or raw disks in some cases, to provide
you maximum flexibility in how you use them. Before you can use a data
disk, you might need to format it, partition it, or group it into a
software RAID group.

To prepare a data disk for use on a cloud server, follow the steps
appropriate for that server's operating system:

* For Linux,
  see
  :how-to:`Preparing Data Disks on Linux Cloud Servers <preparing-data-disks-on-linux-cloud-servers>`.

* For Windows,
  see
  :how-to:`Preparing Data Disks on Windows Cloud Servers <preparing-data-disks-on-windows-cloud-servers>`.

.. TIP::
   To make a backup copy of a *data* disk, use one of the following services:

   * Cloud Backup for incremental backups,
     such as for disaster recovery

   * Cloud Block Storage for portable backups,
     such as for relocation to
     new servers

.. include:: /_common/seealso-concepts-cloud-block-storage.txt
