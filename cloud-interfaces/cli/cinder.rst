.. _cinder:

^^^^^^^^^^
cinder CLI
^^^^^^^^^^
The OpenStack tool primarily used for
managing Cloud Block Storage is written
in Python and called *cinder*.
It is also known as
*python-cinderclient*.

The following OpenStack documents can help you install cinderclient
and learn to use it:

* :os-docs:`Install the OpenStack command-line clients <user-guide/common/cli_install_openstack_command_line_clients.html>`

* :os-docs:`OpenStack Command-Line Interface Reference <cli-reference/content/index.html>`,
  especially at
  :os-docs:`Block Storage command-line client <cli-reference/content/cinderclient_commands.html>`

* :os-docs:`cinder CLI man page <developer/python-cinderclient/man/cinder.html>`

You can use cinder to back up your volumes to :ref:`swift`, the OpenStack tool
used to interact with Cloud Files. For more information about how to back up
your cinder volumes, see
:rax-dev:`Backing up cinder volumes to swift <blog/backing-up-cinder-volumes-to-swift/>`.

.. include:: /_common/note-openstack-username.txt
