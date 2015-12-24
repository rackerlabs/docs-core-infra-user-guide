.. _troubleshoot:

----------------------------
Troubleshooting in the cloud
----------------------------
Many of the same troubleshooting skills you already know apply
to the Rackspace cloud as well.

When you run into a problem, try to eliminate as many unknowns
as possible. Try to get the simplest possible example of what you
want to achieve working first.

However, there are specific areas
that may be new to you. Here are some tips which may help you
if you run into issues:

Troubleshooting connectivity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Connectivity issues can relate to
client-to-server or server-to-server connections.
They can also relate to connections among cloud services.

----

**Symptom:**
An attempt to connect to a server fails.

**Test 1:**
Try reaching the same server from different network locations,
devices, and directions.

**Diagnosis 1:**
If any method succeeds in connecting to the server,
the problem is not in the server itself
but in some aspect of the network.

**Test 2:**
Try to access the server by
its IP address
(for example, 192.0.2.0)
instead of its
DNS entry (for example, www.example.com).

**Diagnosis 2:**
If the server is accessible by its IP address but not by its DNS entry,
the problem relates to the DNS rather than
to the server itself.

**Test 3:**
Try to confirm basic TCP/IP connectivity by using
`telnet <https://tools.ietf.org/html/rfc854>`__.

**Diagnosis 3:**
If you cannot telnet to a target IP through a target port,
a :kc-article:`firewall <introduction-to-firewalls>`
may be blocking your access.

----

**Symptom:**
An attempt to connect between Cloud Servers and another cloud service fails.

**Test and prevention:**
Follow the guidance at :ref:`network-ssh` to
determine how your SSH port should be configured
to enable cloud services to interact.

----

.. seealso::
   To learn more about troubleshooting or preventing connectivity issues,
   read these articles:

   * :kc-article:`Basic network troubleshooting <basic-network-troubleshooting>`

   * :kc-article:`Troubleshooting DNS issues <troubleshooting-dns-issues>`

   * :kc-article:`Introduction to firewalls <introduction-to-firewalls>`

   * :ref:`network-ssh`


Troubleshooting servers
~~~~~~~~~~~~~~~~~~~~~~~
* Keep in mind that Windows servers normally take
  longer to build than other operating systems.

* If a build fails, try again. The build system is often
  busy and doesn't always succeed; try more than once before being
  sure of a problem.

Other troubleshooting resources
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Rackspace provides a
`real-time system status view <https://status.rackspace.com>`__
that may help you understand whether a problem is unique to you or
is caused by something more general.

You can also subscribe to our
`@Rackstatus <https://twitter.com/rackstatus>`__
Twitter feed for updates on maintenance or
other service-impacting events.

As a managed cloud company, we're always available for you to
contact us directly. If you need help, you can reach out to us
through the "Support"
link at the top of the
:mycloud:`Rackspace Cloud Control Panel <>`.
