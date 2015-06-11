.. _bestpractice:

---------------------------
Best practices in the cloud
---------------------------
As you learn about and experiment with the many options 
available to you in the Rackspace Cloud, 
remember these general suggestions 
as tried-and-true best practices:

* Assume failure can happen and design accordingly. Don't rely on 
  individual resources 
  such as VMs and storage to always be available.

* Decompose your application into smaller individually scalable parts.
  Don't have a monolithic server that scales up as your demand grows.

* When you must stop or reboot an active server, 
  always do so via the operating system.
  Using the control panel to 
  initialize a running server 
  can lead to data loss and should generally be avoided.

* Deploy a load balancer to allow you to more easily scale and
  update your application. 
  Follow the configuration guidelines at 
  `Configuring a Load Balancer <http://www.rackspace.com/knowledge_center/article/configuring-a-load-balancer>`_.

* Deploy backup and/or monitoring for your most important servers. 
  Configure Cloud Backup as discussed at 
  `Rackspace Cloud Backup - Overview <http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview>`_.

Other best practices relate to specific services, options, 
and configurations:

Best practices for orchestration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*  Always configure services and applications to restart upon reboot.

*  Use config drive and cloud-init to bootstrap your servers 
   as described at
   `Using Cloud-init with Rackspace cloud <https://developer.rackspace.com/blog/using-cloud-init-with-rackspace-cloud/>`_.

*  For Cloud Images, use the UUID where possible because the UUID
   of an image cannot change, whereas the name cannot be guaranteed
   to be constant.

*  Use base images rather than snapshots for build-time performance.

*  Automate configuration tasks whenever possible.

Best practices for security
~~~~~~~~~~~~~~~~~~~~~~~~~~~
*  Sending a high volume of email from your Cloud Server can downgrade
   its IP reputation; use Mailgun instead, 
   as described at 
   `Mailgun Quickstart <https://documentation.mailgun.com/quickstart-sending.html#how-to-start-sending-email>`_.

*  Use SSH keys rather than passwords for Linux. 
   Follow the procedure at 
   `Basic Cloud Server Security <http://www.rackspace.com/knowledge_center/article/basic-cloud-server-security>`_.

Best practices for storage 
~~~~~~~~~~~~~~~~~~~~~~~~~~
* Use attached storage whenever possible since it will allow you to
  resize, backup, and plan for failure more gracefully. 
  Follow the tutorial at 
  `Create and Attach a Cloud Block Storage Volume <http://www.rackspace.com/knowledge_center/article/create-and-attach-a-cloud-block-storage-volume>`_.

Best practices for networking
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*  Use 
   `ServiceNet <http://www.rackspace.com/knowledge_center/frequently-asked-question/what-is-servicenet>`__ 
   to communicate between Cloud Servers and Cloud Files and Cloud Databases. 
   Use Cloud
   Networks for server-to-server communication.

*  For Cloud Networks, use `RFC 1918 
   <https://tools.ietf.org/html/rfc1918>`_ less the two 
   ServiceNet blocks.
