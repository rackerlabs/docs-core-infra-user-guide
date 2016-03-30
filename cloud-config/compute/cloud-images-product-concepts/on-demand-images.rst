.. _on-demand-images:

~~~~~~~~~~~~~~~~
On-demand images
~~~~~~~~~~~~~~~~
When you use the Cloud Control Panel or the Cloud Servers API to create
an image of one of your servers, you get a copy of your
server's system disk. The image does not include any server state stored
in memory, and for flavors that contain more than one disk, it does not
include the data disk or disks. Thus an on-demand image is not really a server
backup; it is more of a template that you can use to create other
servers just like the one you already have.

When you create an on-demand image of your server, ensure
that any running applications have their states saved to disk before you
create the snapshot. Otherwise, these applications might not start
correctly when you boot a server from the image. The time that such
applications should be quiesced is fairly brief and can be monitored by
observing your Cloud Server's task state.
For more information, see
:how-to:`Using Task States with Server Imaging <using-task-states-with-server-imaging>`
in  Rackspace How-To.

.. include:: /_common/seealso-concepts-cloud-images.txt
