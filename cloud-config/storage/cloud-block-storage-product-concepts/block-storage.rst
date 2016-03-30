.. _block-storage:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Block storage for cloud servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Using Cloud Block Storage, you can add disk space to your cloud
servers by attaching storage volumes.

Cloud Block Storage offers volumes in the following flavors:

* Standard (spinning hard disk, or SATA)

* High-performance (SSD)

Standard (SATA) volumes are suitable for customers who need traditional
high-capacity storage at a low price. SSD volumes are suitable for
customers who intend to run databases or other highly transactional or
high-I/O applications in the cloud.

Cloud Block Storage for OnMetal servers
'''''''''''''''''''''''''''''''''''''''
If you need more than 32 GB of storage, but do not have a
requirement for the fast I/O normally provided by an OnMetal server,
you can connect your OnMetal server to a Cloud Block Storage volume.

Connecting your OnMetal server to a Cloud Block Storage volume is
particularly useful for OnMetal Compute and Memory v1 flavors.

To learn how to attach a volume to your OnMetal server, begin
with
:how-to:`Attach a Cloud Block Storage Volume to an OnMetal server <attach-a-cloud-block-storage-volume-to-an-onmetal-server>`.

.. include:: /_common/seealso-concepts-cloud-block-storage.txt
