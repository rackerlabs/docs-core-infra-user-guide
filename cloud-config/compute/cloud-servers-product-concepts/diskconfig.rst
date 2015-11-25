.. _diskconfig:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Configuring disks for a cloud server
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
When you create a cloud server, it is provisioned on a physical server
in a RAID 10 configuration. This configuration provides a level of underlying
redundancy without requiring you to invest extra configuration effort.

Persistent and ephemeral disks
''''''''''''''''''''''''''''''
The type and number of disks presented to a flavor can vary from class
to class. Local disks can be persistent, or a mix of persistent and
ephemeral. Both kinds of disks are protected from failure of the
underlying hardware by RAID 10. If a server fails, the data on its
ephemeral disk persists.

Persistent disks persist through user-initiated actions against a
server; ephemeral disks do not. For example, if a snapshot action is
initiated against a cloud server, it copies the persistent disk, but any
data on an ephemeral disk is not copied.

Depending on the interface used, persistent and ephemeral disks are
labeled differently:

* The Cloud Servers API labels the persistent disk as ``Disk`` and the
  ephemeral disk as ``Ephemeral``.

* The Cloud Control Panel labels the persistent disk as ``System Disk`` and
  the ephemeral disks as ``Data Disk``.

Presentation of disks to the operating system
'''''''''''''''''''''''''''''''''''''''''''''
A flavor may have zero or multiple individual disks presented to it.
Additional disks are supplied unformatted and without a partition. Some
behavior varies with the operating system:

* Linux labels the system disk ``/dev/xvda``. Subsequent disks are
  labeled starting at ``/dev/xvde`` and proceeding through the alphabet
  for each additional local disk or attached Cloud Block Storage
  volume.

* Windows requires that the disk is brought online, a drive letter
  is assigned to it, and the disk is formatted.

Manual and automated disk configuration
'''''''''''''''''''''''''''''''''''''''
Linux PVHVM images use cloud-init to format and expand the system disk’s
root partition to fill the entire available drive space at boot. All
other Linux images use the additional **Disk Configuration** setting to
control this behavior:

* **Auto**: The additional drive space is formatted and the root
  partition is expanded to fill the entire system disk. This is the
  default option.

* **Manual**: The root partition is left unchanged and any additional
  space on the system disk is left unformatted and un-partitioned.

The manual setting results in a faster boot time for the server, because
formatting adds additional time to the boot process. It also allows a
higher degree of customization of the disk.

This option is not available for Windows.

.. include:: /_common/seealso-concepts-cloud-servers.txt
