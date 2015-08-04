.. _security:

-------------------
Tightening security
-------------------
Every time you create a server, whether in the cloud or in your data
center, configure it to disable abuse and enable your
legitimate work. You might need to do some research to identify the
specific steps required to secure your configuration, but the steps
should be similar to those shown in
:kc-article:`Basic Cloud Server Security <basic-cloud-server-security>`,
which demonstrates the process of securing a cloud server running
Ubuntu. For that server, the steps are as follows:

1.  Edit the SSH **known\_hosts** file and remove entries that point to your
    server's IP address.

2.  Change your root password.

3.  Add an admin user.

4.  Give the admin user sudo privileges.

5.  Establish a public/private key.

6.  Set permissions for the key.

7.  Disable unused ports.

8.  Establish a firewall.

9.  Set rules for the firewall.

10.  Create a script to activate the firewall after every restart.

Similar steps for securing cloud servers running operating systems
based on Debian and Red Hat
Package Manager (RPM) are described in the Cloud Launch Guide
tutorial for
`Securing a Cloud Server <https://launch.rackspace.com/guides/securing-server>`__.

.. TIP::
   Because security configuration can be time-consuming, it's a good idea
   to save a copy of a clean, securely-configured cloud server that works
   well for your purpose.
   You can use Cloud Images to maintain a consistent starting point
   for future servers that you create.

Security-related offerings from Rackspace partners are listed in the
`Rackspace Marketplace <https://marketplace.rackspace.com/home#!category/41>`__.
You might find one or more of these that directly addresses your specific
security needs.
