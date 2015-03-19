.. _cloud_servers_product_actions:

=========================
Actions for Cloud Servers
=========================
The following actions can be performed against an active, running server in the
Control Panel and the API.

Note: Depending on your user's specific permissions, you may be unable to access
all of these actions.

To learn how to perform Cloud Servers actions using your choice of interface, 
begin at 

* :ref:`cloudservers_GUI`
* :ref:`cloudservers_CLI`
* :ref:`cloudservers_API`

Rebuild
-------
This action rebuilds a server on the same physical host with a selected base
image or saved snapshot. The image you select must be within the same operating
system family (Windows or Linux). You will retain your public and ServiceNet IP
addresses. All data and disk formatting is lost.

Resize
------
Note: This action is not available for all flavor classes. Due to the
presentation of the disks the option may be limited to up only or disallowed
entirely.

The resize action allows a server to sized up or down within the same flavor
class. The server is offline during the resize. A new server on a different
physical host is reserved and data is then copied from the source to the
destination. Once all of the data has been transferred and the public and
private IPs have been remapped the newly sized server is brought online. You are
then asked to confirm the resize within the next 24 hours by checking to make
sure your server is working as intended. Confirming destroys the original source
server; reverting moves you back to it. After 24 hours, your resize will be
automatically confirmed.

Rescue Mode
------------------
Rescue mode builds a new server using the current server's image. If the system
is unable to access the current server's image then it will use the base image
that server was built from. For example, if you have a server running a CentOS
6.5 snapshot with changes you have created it will attempt to use that snapshot.
If that snapshot is no longer available it will use the base CentOS 6.5 image.

Upon entering Rescue Mode a temporary password will be issued to login to the
server. At this point you can access the file system to recover or troubleshoot
any issues. The exact process varies based on the operating system.

Rescue mode can be exited at any time returning your VM to its original state
with any changes made. Rescue mode will be automatically exited after 24 hours.
 
Reboot
------
This action performs a soft or hard reboot of the server.

Soft Reboot
^^^^^^^^^^^
A soft reboot is a graceful shutdown and restart of the server's operating
system.

Hard Reboot
^^^^^^^^^^^
A hard reboot power cycles your server, which performs an immediate shutdown and
restart.

Console
-------
This action will open a Java web terminal emulator window with a login prompt to
the server over a secure HTTPS connection. This allows access to the server when
access from SSH or RDP might be inhibited due to the server's configuration or
an error state. It might be necessary to install or update Java on the web
browser used to access the console or to switch web browsers to ensure proper
operation. The console is a backup means to access a server and should not be
the primary method of access.

Rename
------
This action changes the label for how a server is named in the Control Panel and
via the API. This does not actually change the hostname on the server itself.

Delete
------
This action permanently deletes a server. Latent data is not recoverable from
the disk of a deleted server.
