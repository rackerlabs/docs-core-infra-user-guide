.. _on-demand_images:

''''''''''''''''
On-demand images
''''''''''''''''
When you use the Cloud Control Panel or the Cloud Servers API to create
an image of one of your Cloud Servers, you get a copy of your Cloud
Server's system disk. The image does not include any server state stored
in memory, and for flavors containing more than one disk, it will not
include the data disk(s). Thus an on-demand image is not really a server
backup. It is more of a template that you can use to stamp out other
Cloud Servers just like the one you're already using.

When you create an on-demand image of your server, you need to be sure
that any running applications have their states saved to disk before you
create the snapshot. Otherwise, these applications may not start
correctly when you boot a server from the image. The time such
applications should be quiesced is fairly brief and can be monitored by
observing your Cloud Server's task state. 
See `Using Task States With Server
Imaging <http://www.rackspace.com/knowledge_center/article/using-task-states-with-server-imaging>`__
in the Rackspace Knowledge Center for details.
