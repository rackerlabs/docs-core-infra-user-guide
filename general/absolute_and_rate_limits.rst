Absolute and Rate Limits
========================
Enforcing limits on some activities 
makes it easier to control costs. 
Because you pay for only what you use
in the Rackspace cloud, 
limits mean you won't be surprised by 
a sudden spike in billable activity. 
Limits can also protect you from 
workloads beyond the capacity of your
configuration. 

Limits on your account's activity 
are initially set by Rackspace. 
You can change some limits 
yourself to suit your workload; 
to change other limits, contact Rackspace.

Absolute limits
---------------
Absolute limits control the total number of 
the limited item that the user can possess simultaneously.

For example, an absolute limit controls the amount of RAM that can
be assigned in a server configuration.

Rate limits
-----------
Rate limits control the frequency at which 
the user can issue specific requests. 
Rate limits are reset after a certain amount of time passes. 

For example, a rate limit controls the number of GET 
requests that can be processed during a
one-minute period.

Limits for specific services
----------------------------
This table shows some examples of limits, 
with links to API documentation for 
more examples and complete details.

+--------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------+
| Service            | Absolute limit example                                                                                             | Rate limit example                                                                                            |
|                    |  (click to see more)                                                                                               |  (click to see more)                                                                                          |
+====================+====================================================================================================================+===============================================================================================================+
|Cloud Block Storage |`10 TB in config <http://docs.rackspace.com/cbs/api/v1.0/cbs-devguide/content/Absolute_Limits-d1e1397.html>`_       |no limits                                                                                                      | 
+--------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------+
|Cloud Servers       |`100 servers in config <http://docs.rackspace.com/servers/api/v2/cs-devguide/content/Absolute_Limits-d1e994.html>`_ |`100 POSTs per minute <http://docs.rackspace.com/servers/api/v2/cs-devguide/content/Rate_Limits-d1e862.html>`_ | 
+--------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------+
|Cloud Images        |no limits                                                                                                           |no limits                                                                                                      | 
+--------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------+
|Cloud Networks      |no limits                                                                                                           |no limits                                                                                                      | 
+--------------------+--------------------------------------------------------------------------------------------------------------------+---------------------------------------------------------------------------------------------------------------+

.. NOTE::
   The services discussed here are not the only ones 
   with absolute limits or rate limits.
   Some services have no limits. 
   We publish the limits relevant to any service 
   in that service's 
   API documentation. You can find those details
   by going to http://docs.rackspace.com/
   and searching for "limits". 
