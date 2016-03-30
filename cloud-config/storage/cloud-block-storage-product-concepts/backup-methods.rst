.. _backup-methods:

~~~~~~~~~~~~~~
Backup methods
~~~~~~~~~~~~~~
The virtual storage presented to your cloud server is backed by physical
hardware in RAID 10 configurations. RAID 10 means that multiple physical
disks in the same physical host would have to fail before there would be
a chance of data loss on your server. Extensive hardware failure
of this nature is extremely unlikely, especially within the protective
environment of Rackspace data centers, but you might still be at risk for
data loss caused by human errors or human malice.

Rackspace **strongly recommends** that you use one or more of the
following methods to create and manage backup copies
of your system and data
disks, providing an extra layer of protection and recoverability for
your cloud servers.

Backup method: snapshots
''''''''''''''''''''''''
You can create snapshots (also known as saved images or server images)
by using the API or Cloud Control Panel. Snapshots save a complete copy of
your system disk. The image is saved in your account and you can
build a new cloud server from the image.

**Data disks are not captured when you create snapshots**.
Only the system
disk is captured.
You should use additional forms of backup if your data
disks hold critical data that must be protected.

Backup method: Cloud Backup
'''''''''''''''''''''''''''
Cloud Backup is a file-based backup application that enables you
to choose
which files and folders to back up from your server. If you have
created a backup copy of your data, you can restore all your
folders and files from the backup, you can restore individual files
or folders from a given date, or you can restore to an entirely different
server. For more information about Cloud Backup, begin at
:how-to:`Rackspace Cloud Backup - Overview <rackspace-cloud-backup-overview>`.

Backup method: Cloud Block Storage
''''''''''''''''''''''''''''''''''
You can use Cloud Block Storage to create and manage disk images that
are portable among your cloud servers. Cloud Block Storage is part of
our core infrastructure; learn more about it at
:ref:`cloud-block-storage-product-concepts`.

Backup methods: custom
''''''''''''''''''''''
You can establish a custom backup process by using a utility such as
`rsync <https://rsync.samba.org/>`__, an open-source utility that
provides fast incremental file transfer.

Storage-related offerings from Rackspace partners are listed in the
`Rackspace Marketplace <https://marketplace.rackspace.com/>`__.
You might find one or more of these
that directly addresses your specific needs.

.. include:: /_common/seealso-concepts-cloud-block-storage.txt
