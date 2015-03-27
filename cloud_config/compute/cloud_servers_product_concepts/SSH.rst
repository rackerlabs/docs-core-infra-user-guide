.. _SSH:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Managing access with SSH Keys
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
SSH keys allow a user to manage and assign RSA keys for the root user to
a server at build from the API or the control panel.

Key names are associated with a public and private key pair in the API
and the control panel. A key pair may be created or an existing public
key uploaded and associated with a key name. If a new key pair is
created the private key will be saved as a *.pem* suffixed file.

SSH keys are stored per region. For example, a key stored in DFW will
not be usable in IAD unless it is also added there. SSH keys may be
listed, viewed, and deleted via the API or the control panel.

.. Note:: SSH keys only work in conjunction with a server 
   running Linux and
   are not compatible with Windows. 
   Although the API will allow a Windows
   server to be built with a key, the key will be non-functional.
