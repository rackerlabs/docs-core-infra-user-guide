Disk Configuration
==================

The disks on a physical server a cloud server is provisioned on are in a Raid 
10 configuration. This provides a level of underlying redundancy without extra
configuration on the part of the user.  

Persistent and Ephemeral
------------------------
The type and number of disks presented to a flavor can vary from class to 
class. Local disks will always be Persistent, or a mix of Persistent and 
Ephemeral. Both are protected from failure of the underlying hardware by
Raid 10, if a cloud server fails the data on the Ephemeral disk will persist.

Any Persistent disks will persist through user initiated actions against a
server, Ephemeral disks are not. For example if the snapshot action is 
initiated against a server it will only copy the Persistent disk, any data
on the Ephemeral disk is not copied.

Depending on the interface used Persistent and Ephemeral disks can be labeled
differently. The API labels Persistent as 'Disk' and Ephemeral as 'Ephemeral',
in the Cloud Control Panel Persistent is 'System Disk' and Ephemeral is 'Data 
Disk'. 

Presentation of disks to OS
---------------------------
A flavor may have 0 or multiple individual disks presented to it, additional
disks are supplied unformatted and without a partition. 

Linux
^^^^^
For Linux the System Disk will be labeled '/dev/xvda', subsequent disks will 
start at '/dev/xvde' and carry on through the alphabet for each additional
local disk or attached Cloud Block Storage volume.

Windows
^^^^^^^
Windows will require that the disk be brought online, a drive letter assigned, 
and the disk formatted.

Manual and Auto Disk Configuration
----------------------------------
Linux PVHVM images utilize cloud-init to format and expand the System Disk's
root partition to fill the entire available drive space at boot. All other
Linux images carry the additional **Disk Configuration** setting to control
this behavior.

**Auto** - The additional drive space is formatted and the root partition is 
expanded to fill the entire System Disk. This is the default option.

**Manual** - The root partition is left unchanged, any additional space on the
System disk is left unformatted and un-partitioned.

Manual results in a faster boot time for the server as formatting adds 
additional time to the boot process. It also allows a higher degree of 
customization of the disk.

This option is not available for Windows.
