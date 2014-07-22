Actions
=======
Actions represent any of the below listed actions that can be taken against an active running server from the API or Control Panel.

Rebuild
------------------
Rebuilds a server on the same physical host with a selected base image or saved snapshot. Must be within the same OS family (Windows, Linux). Retains your public and service net IP. All data and disk formatting is lost.

*How does this works for diskless and OnMetal?*

Resize
------------------
Resize is not available for all flavor classes, due to the presentation of the disks the option may be limited to up only or disallowed entirely. 

Allows a server to sized up or down within the same flavor class. The server is offline during the move. This reserves the new sized server on a different physical host and then copies the data from the source to the destination. Once all of the data has been transferred and the public and private IP's remapped the newly sized server is brought online. During this time you are asked to confirm the resize by checking to make sure your server is working as intended. Confirming destroys the original source server, reverting moves you back to it.

*How this works with BFV and floating IPs?*



Rescue Mode
------------------
Reboot
------------------
Console
------------------
Rename
------------------
Delete
------------------
