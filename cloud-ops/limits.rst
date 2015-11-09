.. _limits:

-------------------------------
Managing your Rackspace account
-------------------------------
When you log in to your :mycloud:`Cloud Control
Panel <>`, you can examine and change
your managed cloud configuration. For example, you can create a cloud
server or delete a block storage volume.
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
(:kc-article:`RBAC <overview-role-based-access-control-rbac>`),
you can divide responsibilities among members of your team. For
example, you can enable a database administrator to schedule database
backups and enable a network administrator to expand a load balancing
group. The roles that make sense for your team are likely to change as
your workload grows, your team grows, and you add more services to your
configuration. You can see suggested role configurations at
:kc-article:`Managing: Role-Based Access Control (RBAC) <managing-role-based-access-control-rbac>`.

Managing expenses by limiting workload
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Enforcing limits on some activities makes it easier to control costs.
Because you pay for only what you use in the Rackspace Managed Cloud,
limits mean that you will not be surprised by a sudden spike in billable
activity. Limits can also protect you from workloads beyond the capacity
of your configuration.

Limits on your account's activity are initially set by Rackspace. You
can change some limits yourself to suit your workload; to change other
limits, contact Rackspace.

Absolute limits
^^^^^^^^^^^^^^^
Absolute limits control the total number of service resources that the
user can possess simultaneously. For example, an absolute limit
controls the amount of RAM that can be
assigned in a Cloud Servers configuration.

Default absolute limits are set to provide you with a reasonable
amount of resources for testing and moderately-sized environments
and applications. If you need additional resource capacity, you
can request an increase of your absolute limits by opening a
ticket in the Cloud Control Panel or by contacting Rackspace Support.

When you are logged in to the Cloud Control Panel,
you can see absolute limits defined for servers,
along with your current consumption of the limited resources,
by clicking the **Account: yourUserName** menu and selecting
:mycloud:`Resource Limits <account#resource-limits>`.

Rate limits
^^^^^^^^^^^
Rate limits control the frequency at which the user can issue specific
requests. Rate limits are reset after a certain amount of time passes.
For example, a rate limit controls the number of GET requests that can
be processed during a one-minute period.

Default rate limits are set such that most users won't encounter them,
however if needed, you can raise your rate limits by opening a ticket in
the Cloud Control Panel or by contacting Rackspace Support.

Limits for specific services
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The following table shows some examples of limits, with links to API
documentation for more examples and complete details.

+-----------------------+-------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------+
| **Service**           | **Absolute limit example**                                                                                              | **Rate limit example**                                                                   |
+=======================+=========================================================================================================================+==========================================================================================+
| Cloud Block Storage   | :rax-dev-devguide:`10 TB in config <cloud-block-storage/v1/developer-guide/#document-general-api-info/absolute-limits>` | No limits                                                                                |
+-----------------------+-------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------+
| Cloud Servers         | :rax-dev-devguide:`100 servers in config <cloud-servers/v2/developer-guide/#absolute-limits>`                           | :rax-dev-devguide:`100 POSTs per minute <cloud-servers/v2/developer-guide/#rate-limits>` |
+-----------------------+-------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------+
| Cloud Images          | No limits                                                                                                               | No limits                                                                                |
+-----------------------+-------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------+
| Cloud Networks        | No limits                                                                                                               | No limits                                                                                |
+-----------------------+-------------------------------------------------------------------------------------------------------------------------+------------------------------------------------------------------------------------------+

The services mentioned here are not the only ones with absolute limits
or rate limits. Some services have no limits. We publish the limits
relevant to any service in that service's API documentation. You can
find those details by going to
:rax-docs:`Rackspace Cloud Technical Documentation <>`
and searching
for *limits*.

You can also avoid surprises in your usage-based billing with the help
of several tools:

*  In the :mycloud:`Cloud Control Panel <>`,
   check current usage frequently.

*  Combine Cloud Monitoring and `Cloud
   Intelligence <https://intelligence.rackspace.com/>`__ to help you
   recognize extreme usage peaks.

*  Use Auto Scale to increase resources only when needed.
