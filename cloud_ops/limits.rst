.. _limits:

-------------------------------
Managing your Rackspace account
-------------------------------
When you log into your `Cloud Control
Panel <https://mycloud.rackspace.com/>`__, you can examine and change
your managed cloud configuration. For example, you can create a Cloud
Server or delete a block storage volume. 
You can also examine and change
your account itself in several areas:

*  **Billing and Payments** gives you access to your current balance,
   billing history, billing address, and credit card information.

*  **Usage Overview** shows you today's usage-based billing for the
   current billing cycle, service by service. For Cloud Servers, you can
   see separate subtotals for hourly usage, image storage, and outgoing
   bandwidth.

*  **Account Settings** lets you change the account password, establish
   a security question, enable two-factor authentication, reset your API
   key, and maintain your contact information.

*  **User Management** lets you define users of your account and give
   them specific access, so that some can have full access to the
   account and some can have per-product limitations.

*  **Resource Limits** compares current activity to the limits
   established for your account and provides a method of requesting an
   increase of those limits.

*  **Support Tickets** shows all the open and closed tickets associated
   with your account and provides a method of creating a new ticket.

*  **Upgrade Service Level** identifies the support service level
   currently in effect for your account, compares it to other available
   service levels, and provides a method of requesting more information
   prior to making a change.

Managing role-based access to services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Using role-based access control
(`RBAC <http://www.rackspace.com/knowledge_center/article/overview-role-based-access-control-rbac>`__),
you can divide responsibilities among members of your team, so for
example you can enable a database administrator to schedule database
backups and enable a network administrator to expand a load balancing
group. The roles that make sense for your team are likely to change as
your workload grows, your team grows, and you add more services to your
configuration. You can see suggested role configurations at 
`Managing: Role-Based Access Control (RBAC) <http://www.rackspace.com/knowledge_center/article/managing-role-based-access-control-rbac>`__.

Managing expenses by limiting workload
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Enforcing limits on some activities makes it easier to control costs.
Because you pay for only what you use in the Rackspace managed cloud,
limits mean you will not be surprised by a sudden spike in billable
activity. Limits can also protect you from workloads beyond the capacity
of your configuration.

Limits on your account's activity are initially set by Rackspace. You
can change some limits yourself to suit your workload; to change other
limits, contact Rackspace.

Absolute limits
^^^^^^^^^^^^^^^
Absolute limits control the total number of the limited item that the
user can possess simultaneously.

For example, an absolute limit controls the amount of RAM that can be
assigned in a Cloud Servers configuration.

When you are logged in to the Cloud Control Panel, 
you can see absolute limits defined for Cloud Servers, 
along with your current consumption of the limited resources, 
by clicking your account number and then 
`Resource Limits <https://mycloud.rackspace.com/account#resource-limits>`__. 

Rate limits
^^^^^^^^^^^
Rate limits control the frequency at which the user can issue specific
requests. Rate limits are reset after a certain amount of time passes.

For example, a rate limit controls the number of GET requests that can
be processed during a one-minute period.

Limits for specific services
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This table shows some examples of limits, with links to API
documentation for more examples and complete details.

+-----------------------+------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------+
| **Service**           | **Absolute limit example**                                                                                             | **Rate limit example**                                                                                            |
+=======================+========================================================================================================================+===================================================================================================================+
| Cloud Block Storage   | `10 TB in config <http://docs.rackspace.com/cbs/api/v1.0/cbs-devguide/content/Absolute_Limits-d1e1397.html>`__         | no limits                                                                                                         |
+-----------------------+------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------+
| Cloud Servers         | `100 servers in config <http://docs.rackspace.com/servers/api/v2/cs-devguide/content/Absolute_Limits-d1e994.html>`__   | `100 POSTs per minute <http://docs.rackspace.com/servers/api/v2/cs-devguide/content/Rate_Limits-d1e862.html>`__   |
+-----------------------+------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------+
| Cloud Images          | no limits                                                                                                              | no limits                                                                                                         |
+-----------------------+------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------+
| Cloud Networks        | no limits                                                                                                              | no limits                                                                                                         |
+-----------------------+------------------------------------------------------------------------------------------------------------------------+-------------------------------------------------------------------------------------------------------------------+

The services mentioned here are not the only ones with absolute limits
or rate limits. Some services have no limits. We publish the limits
relevant to any service in that service's API documentation. You can
find those details by going to 
`Rackspace Cloud Technical Documentation <http://docs.rackspace.com/>`__ 
and searching
for *limits*.

You can also avoid surprises in your usage-based billing with the help
of several tools:

*  In the `Cloud Control Panel <https://mycloud.rackspace.com/>`__,
   check current usage frequently.

*  Combine Cloud Monitoring and `Cloud
   Intelligence <https://intelligence.rackspace.com/>`__ to help you
   recognize extreme usage peaks.

*  Use Auto Scale to increase resources only when needed.

Adding services
~~~~~~~~~~~~~~~
If you have never used a service before, 
your first attempt to do so in the Cloud Control Panel 
will remind you that you are beginning something new 
and point out the first step you should take. 

.. image:: ../screenshots/CloudBigData0clusters.png
   :alt: The Cloud Control Panel points out how to begin
         using a new service. 
         

When Rackspace makes a new service generally available, 
all customers are given access to that service. 
When a new service is made available to you, 
its endpoint is added to the 
`service catalog <http://docs.rackspace.com/auth/api/v2.0/auth-client-devguide/content/Sample_Request_Response-d1e64.html>`__ 
that is returned when you authenticate before using an API or CLI.

If you meet eligibility criteria, 
it may be possible for you to experiment with a new service 
before it is made available to all customers. 
The 
`Rackspace blog <http://www.rackspace.com/blog/?s=early+access>`__ 
is a good place to learn about 
limited-access and early-availability releases; 
signup procedures and contact information are included in 
each announcement.  
