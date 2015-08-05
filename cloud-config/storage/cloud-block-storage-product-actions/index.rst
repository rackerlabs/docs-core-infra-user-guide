.. _cloud-block-storage-product-actions:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Actions for Cloud Block Storage
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can use Cloud Block Storage to perform the following actions.

.. include:: /_common/note-rbac-actions.txt

To learn how to perform Cloud Block Storage actions by using your
choice of interface,
begin at one of the following topics:

* :ref:`cloudblockstorage-gui`
* :ref:`cloudblockstorage-cli`
* :ref:`cloudblockstorage-api`

Create a volume
---------------
This action provisions a volume on a Cloud Block Storage storage node. As
part of the volume creation request, you can specify the following
values:

* Volume name

* Description

* Storage type (SATA or SSD)

* Volume size

Immediately after a volume is created, it cannot have any data written
to it. To make the volume available for further operations,
you must attach it to a cloud server.

Attach a volume to a cloud server
----------------------------------
This action creates an iSCSI connection between the storage
node on which the volume resides and the hypervisor of the cloud
server specified in the attachment request.

After attaching the volume to a cloud server, you must partition,
format, and mount it before you can use it. A volume can be attached
only to a
cloud server that resides in the same region as the volume.

Detach a volume from a cloud server
-----------------------------------
This action releases the iSCSI connection between the storage node
and the cloud server hypervisor, and logically
removes the volume as a usable disk for the server.

The detach request can succeed only if the volume is unmounted and
is not in use by the host operating system.

Detaching a volume does not affect data on the volume. User data stored
on Cloud Block Storage volumes is persistent and remains on the volume
even after the volume has been detached from the server.

Create a snapshot of a volume
-----------------------------
This action instructs the Linux Logical Volume Manager (LVM)
Copy on Write (CoW)
mechanism to create consistent point in time snapshots of
Cloud Block Storage volumes.

Snapshots are stored redundantly (three copies) as objects in a backend
master Cloud Files account. Snapshots use data deduplication at the
volume level, so that only the data blocks that have changed since the
last snapshot are uploaded the next time the volume snapshot is taken.

Although not required, we recommended that you detach a volume before
creating a snapshot of it to avoid losing any in-flight data while the
snapshot is being created.

Creating a snapshot of a Cloud Block Storage volume is a two-step process:

1. Create the LVM snapshot on the local storage node.

2. Upload that snapshot to Cloud Files.

After you receive an HTTP 200 status from the snapshot create request, you
can safely reattach the volume and continue normal operation. It is not
necessary to keep the volume detached while the snapshot is being
uploaded to Cloud Files.

Create a volume from a snapshot
-------------------------------
You can create new volumes by using existing snapshots as the source data.
After you create a volume from a snapshot, you can switch the storage
type (SATA or SSD) and increase the volume size. If you increase the
volume size, you must also resize the cloud server file system (if
that action is supported).

Volumes can be created only from snapshots that reside in the same
region as the volume.

Delete a snapshot of a volume
-----------------------------
Deleting a snapshot of a volume removes the objects associated with that
snapshot from Cloud Files.

This action cannot be reversed.

Clone a volume
--------------
Volume cloning enables you to create a new Cloud Block Storage
volume by using an existing volume as the source data.
Although  similar in some aspects to creating a volume from a
snapshot (both use LVM CoW), volume cloning removes Cloud Files
as the intermediary and copies volumes directly between storage nodes.
This provides the ability to make faster copies of volumes. Additionally,
clones are attachable volumes and thus are immediately usable upon
creation. Clones differ from snapshots in this way, because a snapshot
must be restored to a volume before it can be attached to a cloud server
for use.

Delete a volume
---------------
This action deprovisions a volume and deletes the
resulting data from the backend storage node. After a volume has been
deleted, the volume receives a single-pass wipe with zeros before the
blocks are returned to the storage pool and made available for other
customers to use.

A volume cannot be deleted if it is currently attached to a cloud server
or has a dependent snapshot.
