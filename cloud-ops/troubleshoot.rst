.. _troubleshoot:

----------------------------
Troubleshooting in the cloud
----------------------------
Many common-sense practices that help you
recognize, minimize, and prevent trouble in other situations
apply to the Rackspace cloud as well:

* When you encounter a problem, investigate it by eliminating as many unknowns
  as possible. Try to get the simplest possible example of what you
  want to achieve working first. Then introduce new features gradually,
  testing after each change, until you know exactly at which point the
  problem begins.

* Maintain awareness of what is normal and abnormal within your configuration
  and within Rackspace overall. Monitor your systems and maintain historical
  logs so you know when key resources are not operating as usual.

Rackspace provides tools to help you automate detection of and response to
unusual situations such as workload spikes:

* :how-to:`Rackspace Monitoring <cloud-monitoring>`
* :how-to:`Rackspace Auto Scale <rackspace-auto-scale>`
* :how-to:`Rackspace Intelligence <rackspace-intelligence>`

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

.. SEEALSO::

   Although you can generalize basic troubleshooting practices from other kinds of
   computing work, some areas specific to working in the cloud
   may be new to you. Here are some tips which may help you
   understand and address cloud-related issues:

   * :ref:`troubleshoot-connectivity`

     * An attempt to connect to a server fails.
     * An attempt to connect between Cloud Servers and another cloud service fails.

   * :ref:`troubleshoot-build`

     * A cloud server build takes an unusually long time to complete.
     * A cloud server build fails.

----

.. _troubleshoot-connectivity:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~
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
a firewall may be blocking your access.

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

   * :how-to:`Basic network troubleshooting <basic-network-troubleshooting>`

   * :how-to:`Troubleshooting DNS issues <troubleshooting-dns-issues>`

   * :ref:`network-ssh`

.. _troubleshoot-build:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Troubleshooting server builds
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You can build a cloud server much more quickly than you can order a
dedicated server and have it installed and configured.
The build process for cloud servers is rapid but is not instantaneous.
Builds can be delayed by a variety of factors.

----

**Symptom:**
A cloud server build takes an unusually long time to complete.

**Test:**
Identify factors under your control that can explain why this cloud server build
is slower than others you have performed:

* Windows servers take longer to build than
  servers running other operating systems.
* OnMetal servers take longer to build than virtual servers.
* Servers built with software stacks take longer to build than bare servers
  (where a software stack may be installed later).
* Servers built with backup enabled take longer to build than bare servers
  (where a backup capability may be established later).
* Servers built from customer-saved images take longer to build
  than servers built from images provided by Rackspace.

**Diagnosis:**
If any of these known causes of slower builds are true of the server
that you are attempting to build, wait at least thirty minutes before
rechecking for success or failure.
Although build times vary, all server builds eventually
either succeed or fail.

* If a slow server build eventually succeeds,
  use the new server normally.
  A slow build does not predict any operational problems.

* If a slow server build eventually fails,
  investigate the failure just as you would if it had failed quickly.

----

**Symptom:**
A cloud server build fails.

**Test 1:** Check `status.rackspace.com <https://status.rackspace.com/>`_
for any indication that you are being affected by a general problem.

**Diagnosis 1:**
If `status.rackspace.com <https://status.rackspace.com/>`_
identifies any problematic resources that seem relevant to your situation,
look for a **details** link.

.. figure:: /_images/status-disruption-cloudservers.png
   :alt: If you see any status other than "The system is operating normally",
	 look closely to see whether this resource affects you.

   *If you see any status other than "System is operating normally",
   look closely to see whether this resource affects you.*

Click the **details** link, read it carefully, and follow any relevant
instructions offered there.

.. figure:: /_images/status-disruption-cloudservers-detail.png
   :alt: If the details are consistent with your situation,
	 follow instructions there before contacting Support.

   *If the details are consistent with your situation,
   follow instructions there before contacting Support.*

----

**Test 2:**
Try performing the build more than once before being sure of a problem.

**Diagnosis 2:**
If your first build attempt fails but a later build attempt succeeds, this
suggests that the build system was simply too busy during the failed attempt.
This can occur intermittently for brief periods during peak loads;
it does not predict future failures.

If multiple build attempts fail and no general status problems match your
situation, contact Rackspace Support to ask for help.

Many Rackspace pages
offer links to help you begin a live chat session or a telephone conversation
with Support.
:rax:`Contact Rackspace <information/contactus/>`
also provides links to help you submit support tickets.

----

.. seealso::
   To learn more about troubleshooting or preventing server build issues,
   read these articles:

   * :how-to:`RackConnect power users guide <rackconnect-power-users-guide>`
     suggests using the Cloud Servers API to build multiple servers in bursts
     rather than singly.

   * :rax-dev-quickstart:`Set up your first server <cloud-servers/getting-started/#set-up-your-first-server>`
     shows how to use a software development kit (SDK)
     for the programming language of your choice
     to create a cloud server.

   * :ref:`cloud-servers-product-actions`
     identifies actions you can take after a server is built.
     It links to information about how to perform each action with
     the Cloud Control Panel and Cloud Servers API.
