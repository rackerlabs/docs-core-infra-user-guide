.. _time:

~~~~~~~~~~~~~~~~~~~~~~~~~~~
Synchronizing time with NTP
~~~~~~~~~~~~~~~~~~~~~~~~~~~
During boot, Linux sets the cloud server's system clock to the same time
as the physical server's hardware clock. After this initial
synchronization, Linux maintains the server's clock separately
from the hardware clock. If the hardware clock is incorrect, issues can occur
with anything that relies on having the correct time.

Network time protocol (NTP) is an open-source Linux package that enables
a server to synchronize its system clock with a pool of authoritative
NTP servers. You can see a list of public NTP servers at
http://www.ntp.org. By using NTP, you can synchronize the time on your
cloud server with any of the servers on the list.

To install NTP, use the package manager appropriate for your Linux
distribution. When you start NTP, NTP synchronizes the cloud server
with either a default NTP server or an NTP server that you specify. To
specify a different server or set of servers to synchronize with, edit
your NTP configuration file directly.

On a virtual server such as a cloud server, the clock is initially
synchronized with the Xen hypervisor. This means that you must start an
independent clock for NTP to use. Use the following command:

.. code-block:: bash

   echo 1 > /proc/sys/xen/independent_wallclock

To make the independent clock persist through restarts, add the
following to ``*/etc/sysctl.conf*``:

.. code-block:: bash

   #Set independent wall clock time
   xen.independent_wallclock=1

In each region, Rackspace maintains internal NTP servers that cloud
servers can synchronize with:

+--------------+----------------------------+-------------------+
| **Region**   | **Host name**              | **Time zone**     |
+==============+============================+===================+
| DFW          | time.dfw1.rackspace.com    | CST (UTC-06:00)   |
+--------------+----------------------------+-------------------+
| DFW          | time2.dfw1.rackspace.com   | CST (UTC-06:00)   |
+--------------+----------------------------+-------------------+
| ORD          | time.ord1.rackspace.com    | CST (UTC-06:00)   |
+--------------+----------------------------+-------------------+
| ORD          | time2.ord1.rackspace.com   | CST (UTC-06:00)   |
+--------------+----------------------------+-------------------+
| IAD          | time.iad1.rackspace.com    | CST (UTC-06:00)   |
+--------------+----------------------------+-------------------+
| IAD          | time2.iad1.rackspace.com   | CST (UTC-06:00)   |
+--------------+----------------------------+-------------------+
| LON          | time.lon.rackspace.com     | GMT (UTC+00:00)   |
+--------------+----------------------------+-------------------+
| LON          | time2.lon.rackspace.com    | GMT (UTC+00:00)   |
+--------------+----------------------------+-------------------+
| HKG          | time.hkg1.rackspace.com    | HKT (UTC+08:00)   |
+--------------+----------------------------+-------------------+
| HKG          | time2.hkg1.rackspace.com   | HKT (UTC+08:00)   |
+--------------+----------------------------+-------------------+
| SYD          | time.syd2.rackspace.com    | AET (UTC+10:00)   |
+--------------+----------------------------+-------------------+
| SYD          | time2.syd2.rackspace.com   | AET (UTC+10:00)   |
+--------------+----------------------------+-------------------+

.. include:: /_common/seealso-concepts-cloud-servers.txt
