.. _ssh:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Managing access with SSH keys
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
SSH keys enable a user to manage and assign RSA keys for the root user to
a server at build time from the API or the Cloud Control Panel.

Key names are associated with a public and private key pair in the API
and the control panel. You can create a key pair or upload an existing public
key and associate it with a key name. If you create a new key pair,
the private key is saved as a **.pem** suffixed file.

SSH keys are stored per region. For example, a key stored in the DFW region
is not usable in the IAD region unless it is also added there. You can list, view,
and delete SSH keys using the API or the control panel.

.. NOTE::
   SSH keys only work in conjunction with a server
   running Linux and
   are not compatible with Windows.
   Although the API will allow a Windows
   server to be built with a key, the key will not be functional.

.. include:: /_common/seealso-concepts-cloud-servers.txt
