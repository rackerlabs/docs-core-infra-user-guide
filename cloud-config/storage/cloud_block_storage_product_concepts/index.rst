.. _cloud_block_storage_product_concepts:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Understanding Cloud Block Storage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Block Storage (CBS) provides persistent block-level storage
volumes for use with Rackspace Standard and Performance Cloud Servers.
CBS allows customers to scale their storage independently of their
compute resources. 

Cloud Block Storage is based on OpenStack Cinder and leverages
open-source software and commodity hardware components to provide a
low-cost alternative to traditional third-party SAN (storage area
network) vendors. The underlying hardware consists of individual storage
nodes which provide either standard or SSD disks in a protected RAID10
configuration. The distributed storage node system of CBS makes it
horizontally scalable and free from monolithic failure scenarios.

Cloud Block Storage volumes can be provisioned in 1 GB increments,
ranging from 100 GB to 1 TB in size. You can attach up to 10 CBS volumes
per Cloud Server. Volumes are exposed to the hypervisor via iSCSI over a
logical network and are presented to Cloud Servers as virtual devices
(local disks). After a volume is attached to a Cloud Server, you must
prepare the volume for use by partitioning, formatting, and mounting it
through the Cloud Server operating system.

Most Cloud Servers can boot from a network-attached Cloud Block Storage
volume. You can create a bootable CBS volume and launch a server
instance from that volume. Booting from a CBS volume enables disk-less
servers, new server configurations such as high RAM/low storage, and
staging of common server images in CBS.
   
.. TIP::
   For instructions on using CBS boot-from-volume, see
   `Boot a server from a Cloud Block Storage volume <http://www.rackspace.com/knowledge_center/article/boot-a-server-from-a-cloud-block-storage-volume>`__.

The Rackspace Knowledge Center provides many more details about Cloud
Block Storage. Begin exploring
at 
`Cloud Block Storage support <http://www.rackspace.com/knowledge_center/product-page/cloud-block-storage>`__.


Contents:

.. toctree::
   :maxdepth: 2

   disk_storage
   local_storage
   block_storage
   software_RAID
