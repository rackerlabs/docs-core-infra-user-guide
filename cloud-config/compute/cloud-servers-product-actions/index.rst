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

.. seealso::

   Learn how to perform this action with the interface of your choice:

   .. hlist::
      :columns: 3

      * :how-to:`Cloud Control Panel
        <rebuild-a-cloud-server>`
      * :rax-dev-docs:`Rackspace Cloud Servers API
        <cloud-servers/v2/developer-guide/#rebuild-specified-server>`

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

.. NOTE::
   This action is not available for all flavor classes.
   Depending on the
   presentation of the disks, the option might be limited
   to *up* only or disallowed entirely.

.. seealso::

   Learn how to perform this action with the interface of your choice:

   .. hlist::
      :columns: 3

      * :how-to:`Cloud Control Panel
        <managing-your-server-resizing-standard-and-general-purpose-servers>`
      * :rax-dev-docs:`Rackspace Cloud Servers API
        <cloud-servers/v2/developer-guide/#resize-specified-server>`

Rescue
------
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

  .. seealso::

     Learn how to perform this action with the interface of your choice:

     .. hlist::
        :columns: 3

        * :how-to:`Cloud Control Panel
          <rescue-mode>`
        * :rax-dev-docs:`Rackspace Cloud Servers API
          <cloud-servers/v2/developer-guide/#rescue-specified-server>`

Reboot
------
The reboot action performs a soft or hard reboot of the server. A soft reboot is a graceful shutdown and restart of the server's
operating system. A hard reboot power cycles your server, which performs an immediate
shutdown and restart.

.. seealso::

   Learn how to perform this action with the interface of your choice:

   .. hlist::
      :columns: 3

      * :how-to:`Cloud Control Panel
        <reboot-your-server>`
      * :rax-dev-docs:`Rackspace Cloud Servers API
        <cloud-servers/v2/developer-guide/#reboot-specified-server>`

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

.. seealso::

   Learn how to perform this action with the interface of your choice:

   .. hlist::
      :columns: 3

      * :how-to:`Cloud Control Panel
        <start-a-console-session>`
      * :rax-dev-docs:`Rackspace Cloud Servers API
        <cloud-servers/v2/developer-guide/#post-get-console-servers-server-id-action>`

Delete
------
The delete action permanently deletes a server. Latent data is not recoverable
from the disk of a deleted server.

.. seealso::

   Learn how to perform this action with the interface of your choice:

   .. hlist::
      :columns: 3

      * :how-to:`Cloud Control Panel
        <deleting-your-server>`
      * :rax-dev-docs:`Rackspace Cloud Servers API
        <cloud-servers/v2/developer-guide/#delete-delete-server-servers-server-id>`
