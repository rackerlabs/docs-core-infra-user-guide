Actions
=======
Actions represent any of the below listed actions that can be taken against an active running server from the API or Control Panel. Note that these actions may or may not be accessible depending on a users RBAC role.

Rebuild
------------------
Rebuilds a server on the same physical host with a selected base image or saved snapshot. Must be within the same operating system family (Windows, Linux). Retains your public and service net IP. All data and disk formatting is lost.

*How does this works for diskless and OnMetal?*

Resize
------------------
This action is not available for all flavor classes, due to the presentation of the disks the option may be limited to up only or disallowed entirely. 

Allows a server to sized up or down within the same flavor class. The server is offline during the move. This reserves the new sized server on a different physical host and then copies the data from the source to the destination. Once all of the data has been transferred and the public and private IP's remapped the newly sized server is brought online. During this time you are asked to confirm the resize by checking to make sure your server is working as intended. Confirming destroys the original source server, reverting moves you back to it.

*How this works with BFV and floating IPs?*



Rescue Mode
------------------

Builds a new server using the current server's image, if it is unable to determine the current server's image then it will use the base image that server was built from. For example if you have a server running a CentOS 6.5 snapshot with changes you have created it will attempt to use that snapshot. If for some reason it can not use that snapshot it will use the base CentOS 6.5 image.

Upon entering Rescue Mode a temporary password will be issued to login to the server. At this point you can access the file system to recover or troubleshoot any issues, this process differs based on the operating system.

Rescue mode can be exited at anytime returning your VM to it's original state with any changes made, this will automatically happen after 24 hours.
 
Reboot
------------------
This action performs a soft or hard reboot of the server.

Soft Reboot
^^^^^^^^^^^^^^^^^^^^^
A soft reboot is a graceful shutdown and restart of the server's operating system.

Hard Reboot
^^^^^^^^^^^^^^^^^^^^^
A hard reboot power cycles your server, which performs an immediate shutdown and restart.

Console
------------------
This action will open a Java web terminal emulator window with a login prompt to the server over a secure HTTPS connection. This allows access to the server when access from SSH or RDP might be inhibited due to the server's configuration or an error state. It might be necessary to install or update Java on the web browser used to access the console or to switch web browsers to ensure operation. The console is a backup means to access a server and should not be the primary method of access.

Rename
------------------
This action changes the label for how a server is named in the Control Panel and via the API. This does not actually change the server's hostname.

Delete
------------------
This action permanently deletes a server returning it's resources back to the available pool.
