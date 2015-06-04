.. _troubleshoot:

-------------------------
Troubleshooting the Cloud
-------------------------

Many of the same troubleshooting skills you already know apply
to the Rackspace Cloud as well. There are, however, specific areas
which may be new to you. Here are a couple of tips which may help you
run into issues.


Tips and Tricks
~~~~~~~~~~~~~~~

General
-------

* When you run into a problem try to eliminate as many unknowns
  as possible. Try to get the simplest possible example of what you 
  want to achieve working first.

Connectivity
------------

When dealing with connectivity issues, regardless whether they are 
client-to-server or server-to-server, it may be useful to go
through the checklist below.

* Try failing server connections from different network locations,
  devices and directions.

* Try to use the IP address instead of a DNS entry.

* Are you able to use telnet (i.e. telnet TARGET_IP TARGET_PORT) to 
  even just confirm basic TCP/IP connectivity?

* For detailed steps on troubleshooting networking or DNS issues see
  these guides:

  - `Basic Network Troubleshooting (Knowledge Center) 
    <http://www.rackspace.com/knowledge_center/article/basic-network-troubleshooting>`_

  - `Troubleshooting DNS Issues 
    <http://www.rackspace.com/knowledge_center/article/troubleshooting-dns-issues>`_

Servers 
-------

* Keep in mind that Windows servers normally take
  longer to build than other operating systems.

* In case a build fails, try again. The build system is often
  busy and doesn't always succeed, trying multiple times will
  likely succeed.


Other Resources
~~~~~~~~~~~~~~~

If you should suspect a problem with the Rackspace Cloud service in general,
we provide a `real-time system status view <https://status.rackspace.com/>`_.

You may also subscribe to our `@Rackstatus <https://twitter.com/rackstatus>`_ 
Twitter feed for updates on maintenance or other service impacting events. 

As a managed cloud company we're of course always available for you to 
contact us direclty. So please feel free to reach out via the "Support"
link at the top of the `Rackspace Cloud Control Panel 
<https://mycloud.rackspace.com/cloud/>`_.


