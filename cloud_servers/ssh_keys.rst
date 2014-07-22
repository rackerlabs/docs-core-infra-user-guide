SSH Keys
========
Allows a user to manage and assign RSA keys for the root user to a server at build from the API or the control panel. SSh keys only work in conjunction with a server running Linux and are not compatible with Windows. The API will allow a Windows server to be built with a key, however that key is non-functional.

Key names are associated with a public and private key pair in the API and the control panel. A key pair may be created or an existing public key uploaded and associated with a key name. If a new key pair is created the private key will be saved as a *.pem* suffixed file. 

SSH Keys are stored at the region level so a key stored in DFW will not be usable in IAD unless recreated there. SSH keys may be listed, viwewed, and deleted via the API or the control panel.

