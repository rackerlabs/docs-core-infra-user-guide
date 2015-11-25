.. _nova-agent:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Operating a cloud server with nova-agent
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
One of the key differences between a cloud server and a non-cloud
virtual machine (VM) is the presence of nova-agent on the cloud server.

When you create a cloud server for any flavor of Linux or Windows,
nova-agent is installed on the server, along with nova-agent's
prerequisites. For Linux, those prerequisites include
`xe-guest-utilities <http://www.freshports.org/sysutils/xe-guest-utilities>`__.

Normal operation of a cloud server requires nova-agent to remain active.
Disabling or removing nova-agent can have unforeseen consequences to the
operation of a server, and we do not recommend it.

When a cloud server is initialized, nova-agent performs startup
functions such as configuring the server's network, establishing its
hostname, and setting its root or admin passwords.

While a cloud server is operational, nova-agent provides a means of
interacting with the server through the API or the Cloud Control Panel.
Nova-agent enables components outside the server to control the
server by sending messages through the XenStore file system. For
example, when an authorized user of the Cloud Control Panel sends the
server a request to reset its password, the Cloud Control Panel
writes the request to XenStore; nova-agent then reads from XenStore and
informs the server. The hypervisor also reads XenStore, enabling
the hypervisor and the cloud server to maintain consistency where
necessary.

Nova-agent is documented as part of the OpenStack nova project.
Following are some sources of nova-agent documentation provided by
OpenStack:

* :os-wiki:`GuestAgent <wiki/GuestAgent>`

* :os-wiki:`GuestAgent Xenstore Communication <wiki/GuestAgentXenStoreCommunication>`

* :rackerlabs:`OpenStack Unix Guest Agent <openstack-guest-agents-unix>`

* :rackerlabs:`OpenStack Windows Guest Agent for Xenserver <openstack-guest-agents-windows-xenserver>`

.. include:: /_common/seealso-concepts-cloud-servers.txt
