.. _security:

-------------------
Tightening security
-------------------
Every time you create a server, whether in the cloud or in your data
center, configure it to disable abuse and enable your
legitimate work. You might need to do some research to identify the
specific steps required to secure your configuration, but the steps
should be similar to those shown in
:how-to:`Basic Cloud Server Security <basic-cloud-server-security>`,
which demonstrates the process of securing a cloud server running the
Ubuntu operating system. For that server, the steps are as follows:

1.  Edit the SSH **known_hosts** file and remove entries that point to your
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


Limiting network access to your configuration,
so that only legitimate traffic can use pre-defined ports,
is a very effective way of improving overall security.
A firewall is the key tool for this purpose.
Methods not based on firewalls can require you to disable or reassign
connections that are required for normal operation. Before pursuing any of those
methods, consider their implications as described at:

- :ref:`servicenet-publicnet-requirement`
- :ref:`network-ssh`

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
