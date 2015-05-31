.. _security:

-------------------
Tightening security
-------------------
Every time you create a server, whether in the cloud or in your data
center, begin by configuring it to disable abuse and enable your
legitimate work. You may have to do some research to identify the
specific steps required to secure your configuration, but the steps
should be similar to those shown in
`Basic Cloud Server Security <http://www.rackspace.com/knowledge_center/article/basic-cloud-server-security>`__,
which demonstrates the process of securing a Cloud Server running
Ubuntu. For that Cloud Server, the steps are:

*  Edit the SSH known\_hosts file and remove entries that point to your
   Cloud Server's IP address.

*  Change your root password.

*  Add an admin user.

*  Give the admin user sudo privileges.

*  Establish a public/private key.

*  Set permissions for the key.

*  Disable unused ports.

*  Establish a firewall.

*  Set rules for the firewall.

*  Create a script to active the firewall after every restart.

Similar steps for securing Cloud Servers running operating systems 
based on Debian and RedHat
Package Manager (RPM) are described in the Cloud Launch Guide 
tutorial for
`Securing a Cloud Server <https://launch.rackspace.com/guides/securing-server>`__.

.. TIP::
   Because security configuration can be time-consuming, it's a good idea
   to save a copy of a clean, securely-configured Cloud Server that works
   well for your purpose. 
   You can use Cloud Images to maintain a consistent starting point 
   for future Cloud Servers you create.

Security-related offerings from Rackspace partners are listed in the 
`Rackspace Marketplace <https://marketplace.rackspace.com/home#!category/41>`__.
You may find one or more of these that directly addresses your specific
needs.
