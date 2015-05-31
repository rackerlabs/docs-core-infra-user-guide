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

*  Sending a high volume of email from your Cloud Server can downgrade
   its IP reputation; use Mailgun instead.

*  Use config drive and cloud-init to bootstrap.

*  Use base images rather than snapshots for build-time performance.

*  Use SSH keys rather than passwords for Linux.

*  Use ServiceNet for Cloud Files and Cloud Databases; use Cloud
   Networks for server to server communication.

*  For Cloud Networks, use RFC 1918 less the two ServiceNet blocks.

*  For Cloud Images, use the UUID where possible because the UUID
   of an image cannot change, whereas the name cannot be guaranteed
   to be constant.

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
