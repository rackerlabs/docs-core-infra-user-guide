.. _nova:

++++++++
nova CLI
++++++++
The OpenStack tool primarily used for managing Cloud Servers is written
in Python and called *nova*.
It is also known as *novaclient* or
*python-novaclient*.

Rackspace provides some additional functionality on top of the base
OpenStack environment through OpenStack extensions.
To have the
best experience when using the novaclient with Rackspace, you should
install the ``rackspace-novaclient`` package. It will conveniently
install not only the required novaclient componnents, but also any
necessary or useful extensions and plugins that are applicable to the
Rackspace cloud.

We recommend that you use the
`Python Package Index (PyPI) <https://pypi.python.org/pypi>`__
to install novaclient, as it will handle installing dependencies and
required packages for you.

Alternatively, you can download the ``rackspace-novaclient`` package from
the
:rackerlabs:`GitHub repository for rackspace-novaclient <rackspace-novaclient>`.

OpenStack documents that may help you install novaclient
and learn to use it include:

* :os-docs:`Install the OpenStack command-line clients <user-guide/common/cli_install_openstack_command_line_clients.html>`

* :os-docs:`OpenStack Command-Line Interface Reference <cli-reference/content/index.html>`,
  especially at
  :os-docs:`Compute command-line client <cli-reference/content/novaclient_commands.html>`

* :os-docs:`nova CLI man page <developer/python-novaclient/man/nova.html>`

.. include:: note-openstack-username.rst

Rackspace publishes detailed instructions about novaclient,
including how to install the client
on most popular operating systems:

* In the Cloud Servers API documentation at
  :rax-docs:`Install the nova Client with the Cloud Networks Extension <servers/api/v2/cs-gettingstarted/content/section_gs_install_nova.html>`
* In
  :kc-article:`Using python-novaclient with the Rackspace Cloud <using-python-novaclient-with-the-rackspace-cloud>`

After you have novaclient installed, you will need to set up your
environment so you can properly authenticate to Rackspace and use the
tools.
