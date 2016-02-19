.. _bestpractice:

---------------------------
Best practices in the cloud
---------------------------
As you learn about and experiment with the many options
available to you in the Rackspace Cloud,
remember these best practices:

* Assume failure can happen and design accordingly. Don't rely on
  individual resources
  such as VMs and storage to always be available.

* Decompose your application into smaller individually scalable parts.
  Don't have a monolithic server that scales up as your demand grows.

* When you must stop or reboot an active server,
  always do so via the operating system.
  Using the Cloud Control Panel to
  initialize a running server
  can lead to data loss and should generally be avoided.

* Deploy a load balancer to allow you to more easily scale and
  update your application.
  Follow the configuration guidelines at
  :how-to:`Configure a Load Balancer <configure-a-load-balancer>`.

* Deploy backup and/or monitoring for your most important servers.
  Configure Cloud Backup as discussed at
  :how-to:`Rackspace Cloud Backup overview <rackspace-cloud-backup-overview>`.

Other best practices relate to specific services, options,
and configurations:

Best practices for orchestration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*  Always configure services and applications to restart upon reboot.

*  Use config drive and cloud-init to bootstrap your servers
   as described at
   :rax-dev-blog:`Using Cloud-init with Rackspace cloud <using-cloud-init-with-rackspace-cloud>`.

*  For Cloud Images, use the UUID where possible because the UUID
   of an image cannot change, whereas the name cannot be guaranteed
   to be constant.

*  Use base images rather than snapshots for build-time performance.

*  Automate configuration tasks whenever possible.

Best practices for security
~~~~~~~~~~~~~~~~~~~~~~~~~~~
*  Sending a high volume of email from your cloud server can downgrade
   its IP reputation. Use Mailgun instead,
   as described at
   `Mailgun Quickstart <https://documentation.mailgun.com/quickstart-sending.html#how-to-start-sending-email>`_.

*  Use SSH keys rather than passwords for Linux.
   Follow the procedure at
   :how-to:`Basic Cloud Server Security <basic-cloud-server-security>`.

Best practices for storage
~~~~~~~~~~~~~~~~~~~~~~~~~~
* Use attached storage whenever possible because it will allow you to
  resize, backup, and plan for failure more gracefully.
  Follow the tutorial at
  :how-to:`Create and Attach a Cloud Block Storage Volume <create-and-attach-a-cloud-block-storage-volume>`.

Best practices for networking
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*  Use
   :how-to:`ServiceNet <cloud-load-balancers-faq>`
   to communicate between Cloud Servers and Cloud Files and Cloud Databases.
   Use Cloud
   Networks for server-to-server communication.

*  For Cloud Networks, use `RFC 1918
   <https://tools.ietf.org/html/rfc1918>`_, less the two
   ServiceNet blocks.
