.. _cloud_block_storage_product_actions:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Actions for Cloud Block Storage
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You can use Cloud Block Storage to perform the actions described below.

To learn how to perform Cloud Block Storage actions using your choice of interface, 
begin at 

* :ref:`cloudblockstorage_GUI`
* :ref:`cloudblockstorage_CLI`
* :ref:`cloudblockstorage_API`

----

Create a volume
'''''''''''''''
Instructs the Cinder API to provision a volume on a CBS storage node. As
part of the volume creation call, you can specify

* volume name

* description

* storage type (SATA or SSD)

* volume size

Immediately after a volume is created, it cannot have any data written
to it. To make the volume available for further operations, attach it to
a Cloud Server.

Attach a volume to a Cloud Server 
'''''''''''''''''''''''''''''''''
Instructs the Nova API to create an iSCSI connection between the storage
node on which the CBS volume resides and the hypervisor of the Cloud
Server specified in the attachment call.

After attaching the volume to a Cloud Server, you must partition,
format, and mount it prior to use. A volume can only be attached to a
Cloud Server that resides in the same region as the volume.

Detach a volume from a Cloud Server
'''''''''''''''''''''''''''''''''''
Instructs the Nova API to

* release the iSCSI connection between the CBS storage node and the
  Cloud Server hypervisor

* logically remove the volume as a usable disk for the Cloud Server

The detach call can succeed only if the volume is

* unmounted

* not in use by the host operating system

Detaching a volume does not affect data on the volume. User data stored
on Cloud Block Storage volumes is persistent and remains on the volume
even after the volume has been detached from the server.

Create a snapshot of a volume
'''''''''''''''''''''''''''''
Instructs the Linux Logical Volume Manager (LVM) Copy on Write (CoW)
mechanism to create consistent point in time snapshots of CBS volumes.

Snapshots are stored redundantly (3 copies) as objects in a backend
master Cloud Files account. Snapshots utilize data deduplication at the
volume level, so that only the data blocks that have changed since the
last snapshot are uploaded the next time the volume snapshot is taken.

Although not required, it is recommended that a volume be detached prior
to snapshot creation to avoid losing any in-flight data while the
snapshot is being created.

Creating a snapshot of a CBS volume is a two-step process:

1. Create the LVM snapshot on the local storage node.

2. Upload that snapshot to Cloud Files.

After you receive an HTTP 200 status from the snapshot create call, you
can safely reattach the volume and continue normal operation. It is not
necessary to keep the volume detached while the snapshot is being
uploaded to Cloud Files.

Create a volume from a snapshot
'''''''''''''''''''''''''''''''
New volumes can be created using existing snapshots as the source data.
Upon creation of a volume from a snapshot, you can switch the storage
type (SATA or SSD) and increase the volume size. If you increase the
volume size, you must also resize the Cloud Server filesystem (if
supported).

Volumes can only be created from snapshots that reside in the same
region as the volume.

Delete a snapshot of a volume
'''''''''''''''''''''''''''''
Deleting a snapshot of a volume removes the objects associated with that
snapshot from Cloud Files.

This action is unrecoverable; a snapshot cannot be un-deleted.

Clone a volume
''''''''''''''
Volume cloning enables you to create a new CBS volume using an existing
volume as the source data. While similar to volume snapshotting in some
aspects since both utilize LVM CoW, volume cloning removes Cloud Files
as the intermediary and copies volumes directly between storage nodes.
This provides the ability make faster copies of volumes. Additionally,
clones are attachable volumes and thus are immediately usable upon
creation. Clones differ from snapshots in this way, since a snapshot
must be restored to a volume before it can be attached to a Cloud Server
for use.

Delete a volume
'''''''''''''''
Instructs the Cinder API to deprovision a volume and delete the
resulting data from the backend storage node. After a volume has been
deleted, the volume receives a single-pass wipe with zeros before the
blocks are returned to the storage pool and made available for other
customers to use.

A volume cannot be deleted if it is currently attached to a Cloud Server
or has a dependent snapshot.

