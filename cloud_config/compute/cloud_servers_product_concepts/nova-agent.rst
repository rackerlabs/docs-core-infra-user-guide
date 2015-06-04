.. _nova-agent:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Operating a Cloud Server with nova-agent
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
One of the key differences between a Cloud Server and a non-cloud
virtual machine (VM) is the presence of nova-agent on the Cloud Server.

When you create a Cloud Server for any flavor of Linux or Windows,
nova-agent is installed on the Cloud Server, along with nova-agent's
prerequisites. For Linux, those prerequisites include
`xe-guest-utilities <http://www.freshports.org/sysutils/xe-guest-utilities>`__.

Normal operation of a Cloud Server requires nova-agent to remain active.
Disabling or removing nova-agent can have unforeseen consequences to the
operation of a server and it is not recommended.

When a Cloud Server is initialized, nova-agent performs startup
functions such as configuring the server's network, establishing its
hostname, and setting its root or admin passwords.

While a Cloud Server is operational, nova-agent provides a means of
interacting with the server through the API or the Cloud Control Panel.
Nova-agent enables components outside the Cloud Server to control the
Cloud Server by sending messages through the Xenstore file system. For
example, when an authorized user of the Cloud Control Panel sends the
Cloud Server a request to reset its password, the Cloud Control Panel
writes the request to Xenstore; nova-agent then reads from Xenstore and
informs the Cloud Server. The hypervisor also reads Xenstore, enabling
the hypervisor and the Cloud Server to maintain consistency where
necessary.

Nova-agent is documented as part of the OpenStack Nova project. The
following are some sources of nova-agent documentation provided by
OpenStack:

* `GuestAgent <https://wiki.openstack.org/wiki/GuestAgent>`__

* `GuestAgent Xenstore Communication <https://wiki.openstack.org/wiki/GuestAgentXenStoreCommunication>`__

* `OpenStack Unix Guest Agent <https://github.com/rackerlabs/openstack-guest-agents-unix>`__

* `OpenStack Windows Guest Agent for Xenserver <https://github.com/rackerlabs/openstack-guest-agents-windows-xenserver>`__
