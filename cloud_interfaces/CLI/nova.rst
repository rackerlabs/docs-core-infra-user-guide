.. _nova:

++++++++
nova CLI
++++++++ 
Rackspace implemented 
the OpenStack project named "nova" 
as our Next Gen Cloud Servers product.

The OpenStack tool primarily used for managing Cloud Servers is written
in Python and called *nova*. 
It is also known as *novaclient* or
*python-novaclient*.

Rackspace provides some additional functionality on top of the base
OpenStack environment through OpenStack extensions. 
To have the
best experience when using the *novaclient* with Rackspace, you should
install the *rackspace-novaclient* package. It will conveniently
install not only the required novaclient componnents, but also any
necessary or useful extensions and plugins that are applicable to the
Rackspace cloud.

We recommend that you use the 
`Python Package Index (PyPI) <https://pypi.python.org/pypi>`__ 
to install novaclient, as it will handle installing dependencies and
required packages for you.

Alternatively, you can download the rackspace-novaclient package from
the 
`GitHub repository for rackspace-novaclient <https://github.com/rackerlabs/rackspace-novaclient>`__.

OpenStack documents that may help you install novaclient 
and learn to use it include: 

* `Install the OpenStack command-line clients <http://docs.openstack.org/user-guide/common/cli_install_openstack_command_line_clients.html>`__

* `OpenStack Command-Line Interface Reference <http://docs.openstack.org/cli-reference/content/index.html>`__, 
  especially at 
  `Compute command-line client <http://docs.openstack.org/cli-reference/content/novaclient_commands.html>`__ 

* `nova CLI man page <http://docs.openstack.org/developer/python-novaclient/man/nova.html>`__ 

.. include:: note-openstack-username.rst

Rackspace publishes detailed instructions about novaclient, 
including how to install the client
on most popular operating systems:

* in the Cloud Servers API documentation at 
  `Install the nova Client with the Cloud Networks Extension <http://docs.rackspace.com/servers/api/v2/cs-gettingstarted/content/section_gs_install_nova.html>`__
* in the Knowledge Center at 
  `Using python-novaclient with the Rackspace Cloud <http://www.rackspace.com/knowledge_center/article/using-python-novaclient-with-the-rackspace-cloud>`__

After you have novaclient installed, you will need to set up your
environment so you can properly authenticate to Rackspace and use the
tools.