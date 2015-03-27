.. _host_issues:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Handling host-related issues
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A Cloud Server is a virtual server; it resides on a physical host. The
physical host is designed with redundancies for power, network, and disk
to prevent failures to the underlying virtual servers. It may sometimes
be necessary to restart a physical host for maintenance or other issues.
When it is practical to do so, virtual servers are not disrupted when
their physical host is restarted

In many cases, a virtual server can be live-migrated away from its
current physical host to a new one. Live migration to a new physical
host is transparent to the running virtual server and transparent to
users of the running virtual server. If a physical host is in a state
where the virtual servers are down and live migration cannot be used,
Rackspace sends regular communication until the virtual server in
question is up and running.
