.. _nova:

^^^^^^^^
nova CLI
^^^^^^^^
The OpenStack tool primarily used to manage Cloud Servers is written
in Python and is called *nova*.
It is also known as *novaclient* or
*python-novaclient*.

Rackspace adds some additional functionality to the base
OpenStack environment through OpenStack extensions.
To have the
best experience when using the novaclient with Rackspace, you should
install the ``rackspace-novaclient`` package. It
installs the required novaclient components and any
necessary or useful extensions and plugins that are applicable to the
Rackspace cloud.

We recommend that you use the
`Python Package Index (PyPI) <https://pypi.python.org/pypi>`__
to install novaclient because it installs dependencies and
required packages for you.

Alternatively, you can download the ``rackspace-novaclient`` package from
the
:rackerlabs:`GitHub repository for rackspace-novaclient <rackspace-novaclient>`.

The following OpenStack documents can help you install novaclient
and learn to use it:

* :os-docs:`Install the OpenStack command-line clients <user-guide/common/cli_install_openstack_command_line_clients.html>`

* :os-docs:`OpenStack Command-Line Interface Reference <cli-reference/content/index.html>`,
  especially at
  :os-docs:`Compute command-line client <cli-reference/content/novaclient_commands.html>`

* :os-docs:`nova CLI man page <developer/python-novaclient/man/nova.html>`

.. include:: /_common/note-openstack-username.txt

Rackspace publishes the following detailed instructions about novaclient,
including how to install the client
on most popular operating systems:

* In the Cloud Servers API documentation at
  :rax-docs:`Install the nova Client with the Cloud Networks Extension <servers/api/v2/cs-gettingstarted/content/section_gs_install_nova.html>`
* In
  :how-to:`Python-novaclient and the Rackspace Cloud <using-python-novaclient-with-the-rackspace-cloud>`

After you have novaclient installed, you must set up your
environment so that you can authenticate to Rackspace and use the
tools.
