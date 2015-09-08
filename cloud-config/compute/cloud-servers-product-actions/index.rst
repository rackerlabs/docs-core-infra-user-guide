.. _cloud-servers-product-actions:

^^^^^^^^^^^^^^^^^^^^^^^^^
Actions for Cloud Servers
^^^^^^^^^^^^^^^^^^^^^^^^^
You can perform the following actions against an active, running server in the
Cloud Control Panel and the API.

.. include:: /_common/note-rbac-actions.txt

To learn how to perform Cloud Servers actions by using your choice of interface,
begin at the following sections:

* :ref:`cloudservers-gui`
* :ref:`cloudservers-cli`
* :ref:`cloudservers-api`

Rebuild
-------
The rebuild action rebuilds a server on the same physical host with
a selected base image or saved snapshot. The image that you select must be
within the same operating system family (Windows or Linux).
Your public and ServiceNet IP addresses are retained.
All data and disk formatting is lost.

* To find out how to rebuild a server using the Cloud Control Panel click
  `here <http://www.rackspace.com/knowledge_center/article/managing-your-server-rebuild-a-cloud-server>`__.

* To find out how rebuild a server using Rackspace CLI click
  `here <https://developer.rackspace.com/docs/rack-cli/services/servers/#rebuild>`__.

* To find out how to rebuild a server using the API click
  `here <http://api.rackspace.com/api-ref.html#rebuildServer>`__.

Resize
------
The resize action enables a server to sized up or down within the same flavor
class. The server is offline during the resize. A new server on a different
physical host is reserved, and data is transferred from the source to the
destination. After all of the data has been transferred and the public and
private IPs have been remapped, the newly sized server is brought online.
You have 24 hours to confirm the resize by checking to
ensure that your server is working as intended. Confirming destroys
the original source server, while reverting moves you back to it.
After 24 hours, your resize is automatically confirmed.

* To find out how to resize a server using the Cloud Control Panel click
  `here <http://www.rackspace.com/knowledge_center/article/managing-your-server-resizing-standard-servers>`__.

* To find out how to resize a server using Rackspace CLI click
  `here <https://developer.rackspace.com/docs/rack-cli/services/servers/#resize>`__.

* To find out how to resize a server using the API click
  `here <http://api.rackspace.com/#resizeServer>`__.

.. NOTE::
   This action is not available for all flavor classes.
   Depending on the
   presentation of the disks, the option might be limited
   to *up* only or disallowed entirely.

Rescue Mode
------------------
Rescue mode builds a new server by using the current server's image.
If the system is unable to access the current server's image,
it uses the base image that server was built from. For example,
if you have a server running a CentOS 6.5 snapshot with
changes that you have created, the system tries to use that snapshot.
If that snapshot is not available, the system uses the base CentOS 6.5 image.

When a server enters rescue mode, a temporary password is issued for logging
in to the server. At this point, you can access the file system
to recover or troubleshoot any issues. The exact process varies based
on the operating system.

You can exit rescue mode at any time, returning your VM to its original state
with any changes made. Rescue mode is automatically exited after 24 hours.

* To find out how to build a new server in rescue mode using the Cloud Control Panel
  click `here <http://www.rackspace.com/knowledge_center/article/managing-your-server-rescue-mode>`__.

* To find out how to build a new server in rescue mode using the API
  click `here <http://api.rackspace.com/api-ref.html#rescueServer>`__.

Reboot
------
The reboot action performs a soft or hard reboot of the server. A soft reboot is a graceful shutdown and restart of the server's
operating system. A hard reboot power cycles your server, which performs an immediate
shutdown and restart.

- To find out how to reboot a server using the Cloud Control Panel
  click `here <http://www.rackspace.com/knowledge_center/article/managing-your-server-reboot-your-server>`__.

- To find out how to reboot a server using Rackspace CLI
  click `here <https://developer.rackspace.com/docs/rack-cli/services/servers/#reboot>`__.

- To find out how to reboot a server using the API click
  `here <http://api.rackspace.com/#rebootServer>`__.

Console
-------
The console action opens a Java web terminal emulator window with a
login prompt to the server over a secure HTTPS connection.
This action gives you access to the server when access from SSH or
RDP might be inhibited because of the server's configuration or
an error state. It might be necessary to install or update Java on the web
browser used to access the console or to switch web browsers to ensure proper
operation. The console is a backup means to access a server and should not be
the primary method of access.

* To find out how to open a console using the Cloud Control Panel click
  `here <http://www.rackspace.com/knowledge_center/article/managing-your-server-start-a-console-session>`__.

* To find how to retrieve console output for a specified server using the API click
  `here <http://api.rackspace.com/api-ref.html#getConsole>`__.


Delete
------
The delete action permanently deletes a server. Latent data is not recoverable
from the disk of a deleted server.

* To find out how to delete a server using the Cloud Control Panel click
  `here <http://www.rackspace.com/knowledge_center/article/managing-your-server-deleting-your-cloud-server>`__.

* To find out how to delete a server using Rackspace CLI click
  `here <https://developer.rackspace.com/docs/rack-cli/services/servers/#delete>`__.

* To find out how to delete a server using the API click
  `here <http://api.rackspace.com/#deleteServer>`__.
