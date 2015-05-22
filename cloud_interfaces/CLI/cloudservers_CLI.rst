.. _cloudservers_CLI:

------------------------------------------------
Cloud Servers and CLIs: novaclient and supernova
------------------------------------------------
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
`Python Package Index (PyPi) <https://pypi.python.org/pypi>`__ 
to install novaclient, as it will handle installing dependencies and
required packages for you.

Alternatively, you can download the rackspace-novaclient package from 
https://github.com/rackerlabs/rackspace-novaclient.

Detailed instructions about novaclient, 
including how to install the client
on most popular operating systems, is located at
http://docs.rackspace.com/servers/api/v2/cs-gettingstarted/content/section_gs_install_nova.html.

After you have novaclient installed, you will need to set up your
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
install *supernova* via PyPi, or download it directly from 
http://supernova.readthedocs.org/en/latest/.
