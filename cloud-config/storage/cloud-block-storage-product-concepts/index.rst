.. _cloud-block-storage-product-concepts:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Understanding Cloud Block Storage
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Block Storage provides persistent block-level storage
volumes for use with Rackspace cloud servers.
Cloud Block Storage enables customers to scale
their storage independently of their
compute resources.

Cloud Block Storage is based on the OpenStack Block Storage service
(project named cinder) and leverages
open-source software and commodity hardware components to provide a
low-cost alternative to traditional third-party SAN (storage area
network) vendors. The underlying hardware consists of individual storage
nodes that provide either standard or SSD disks in a protected RAID10
configuration. The distributed storage node system of Cloud Block
Storage makes it
horizontally scalable and free from monolithic failure scenarios.

Cloud Block Storage volumes can be provisioned in 1 GB increments,
ranging from 100 GB to 1 TB in size. You can attach up to 10 Cloud
Block Storage volumes
per cloud server. Volumes are exposed to the hypervisor via iSCSI over a
logical network and are presented to servers as virtual devices
(local disks). After a volume is attached to a server, you must
prepare the volume for use by partitioning, formatting, and mounting it
through the server operating system.

Most servers can boot from a network-attached Cloud Block Storage
volume. You can create a bootable Cloud Block Storage volume and launch a server
instance from that volume. Booting from a volume enables diskless
servers, new server configurations such as high RAM/low storage, and
staging of common server images in Cloud Block Storage.

.. TIP::
   For instructions on using the Cloud Block Storage boot-from-volume feature,
   see
   :how-to:`Boot a server from a Cloud Block Storage volume <boot-a-server-from-a-cloud-block-storage-volume>`.

The Rackspace technical documentation provides many more details about Cloud
Block Storage. Begin exploring at 
:how-to:`Cloud Block Storage support <cloud-block-storage>`.

..
.. below, the include provides visible links
.. (these deep levels are all invisible in the navbar)
.. and the toctree controls the next/previous structure
..

.. include:: /_common/seealso-concepts-cloud-block-storage.txt

.. toctree:: :hidden:
   :maxdepth: 2

   disk-storage
   local-storage
   block-storage

   backup-methods
