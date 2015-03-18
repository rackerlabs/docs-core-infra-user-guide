.. _cloud_interfaces_CLI:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
CLI: command-line interfaces and tools
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
As the Rackspace Cloud is based on OpenStack, there are a rich set of
open source command line interfaces (CLIs) available for users who want
to manage their cloud via shell scripts, manual commands, and more.

CLI for Cloud Servers: OpenStack novaclient
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The OpenStack tool primarily used for managing Cloud Servers is written
in Python and called “nova” (or more formally “novaclient” or
“python-novaclient”).

Rackspace provides some additional functionality on top of the base
OpenStack environment through OpenStack extensions. In order to have the
best experience when using the *novaclient* with Rackspace, you should
install the “rackspace- novaclient” package. It will conveniently
install not only the required novaclient componenents, but also any
necessary or useful extensions/plugins that are applicable to the
Rackspace Cloud.

The rackspace-novaclient package can be found at:
https://github.com/rackerlabs/rackspace-novaclient

However, it is recommended that you use the Python Package Index (PyPi)
to install the client, as it will handle installing dependencies and
required packages for you.

A more detailed set of instructions, including how to install the client
on most popular operating systems, is located at:
http://docs.rackspace.com/servers/api/v2/cs-gettingstarted/content/section_gs_install_nova.html.

Once you have the client installed, you will need to set up your
environment so you can properly authenticate to Rackspace and use the
tools.

If you work with multiple Rackspace regions, you may find another tool
called *supernova* to be useful. *supernova* provides a way for you to
provide credentials and connection information for multiple Rackspace
regions, so you can quickly interact with them without changing
environment variables or configurations as you may need to do with
*novaclient*.

While *supernova* is not officially supported by Rackspace, it is
heavily used and generally found to be stable and useful. You can
install *supernova* via PyPi, or locate it at:
http://supernova.readthedocs.org/en/latest/.

CLI for other services
^^^^^^^^^^^^^^^^^^^^^^
Other clients can help you work with Cloud Images (glanceclient), Cloud
Files (swiftclient), and other services. Which clients you need will
depend on what Rackspace services you are using. All are installed and
managed in a similar fashion.

Contents:

.. toctree::
   :maxdepth: 2

   setup_CLI
   cloudservers_CLI
   cloudnetworks_CLI
   cloudimages_CLI
   cloudblockstorage_CLI
   moreinfo_CLI
