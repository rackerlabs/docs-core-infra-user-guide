.. _explore:

-------------------
Exploring the cloud
-------------------
In the cloud, 
you can quickly try something, decide it isn't quite right, 
then try something else. It's a flexible environment, 
but some practices are more reliable than others, 
and you may sometimes need help. 


Best practices
~~~~~~~~~~~~~~
As you learn about and experiment with the many options available to you, 
remember these as
tried-and-true best practices:

General
-------
* Assume failure will happen and design accordingly. Don't rely on 
  individual resources 
  such as VMs and storage to always be available.

* Decompose your application into smaller individually scalable parts.
  Don't have a monolithic server that scales up as your demand grows.

* Deploy a load balancer to allow you to more easily scale and
  update your application. 
  Follow the configuration guidelines at 
  `Configuring a Load Balancer <http://www.rackspace.com/knowledge_center/article/configuring-a-load-balancer>`_.

* Deploy backup and/or monitoring for your most important servers. 
  Configure Cloud Backup as discussed at 
  `Rackspace Cloud Backup - Overview <http://www.rackspace.com/knowledge_center/article/rackspace-cloud-backup-overview>`_.

Orchestration
-------------
*  Use config drive and cloud-init to bootstrap your servers 
   as described at
   `Using Cloud-init with Rackspace cloud <https://developer.rackspace.com/blog/using-cloud-init-with-rackspace-cloud/>`_.

*  For Cloud Images, use the UUID where possible because the UUID
   of an image cannot change, whereas the name cannot be guaranteed
   to be constant.

*  Use base images rather than snapshots for build-time performance.

*  Automate configuration tasks whenever possible.

Security
--------
*  Sending a high volume of email from your Cloud Server can downgrade
   its IP reputation; use Mailgun instead, 
   as described at 
   `Mailgun Quickstart <https://documentation.mailgun.com/quickstart-sending.html#how-to-start-sending-email>`_.

*  Use SSH keys rather than passwords for Linux. 
   Follow the procedure at 
   `Basic Cloud Server Security <http://www.rackspace.com/knowledge_center/article/basic-cloud-server-security>`_.

Storage 
-------
* Use attached storage whenever possible since it will allow you to
  resize, backup, and plan for failure more gracefully. 
  Follow the tutorial at 
  `Create and Attach a Cloud Block Storage Volume <http://www.rackspace.com/knowledge_center/article/create-and-attach-a-cloud-block-storage-volume>`_.

Networking
----------
*  Use 
   `ServiceNet <http://www.rackspace.com/knowledge_center/frequently-asked-question/what-is-servicenet>`__ 
   to communicate between Cloud Servers and Cloud Files and Cloud Databases. 
   Use Cloud
   Networks for server-to-server communication.

*  For Cloud Networks, use `RFC 1918 
   <https://tools.ietf.org/html/rfc1918>`_ less the two 
   ServiceNet blocks.


Keeping up with change
~~~~~~~~~~~~~~~~~~~~~~
Rackspace is growing and we frequently announce new features, new
products, new prices, and other important changes. Here are some good
ways to keep up with the news:

*  Watch for email sent from Rackspace to the email contact associated
   with your Rackspace account.

*  Read Rackspace blogs, both the 
   `general-interest blog <https://www.rackspace.com/blog/>`__ 
   and the 
   `developer blog <https://developer.rackspace.com/blog/>`__.
   
*  Subscribe to relevant discussion forums in the 
   `Rackspace Community <https://community.rackspace.com/products/f/forumsubscriptions>`__. 

*  Suggest new ideas, vote for development of your favorite ideas, 
   and monitor progress at 
   `Rackspace Product Feedback <https://feedback.rackspace.com/>`__.

*  Follow the 
   `Rackspace twitter feed <https://twitter.com/rackspace>`__.
