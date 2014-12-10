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
Absolute limits control the total number of specific objects that the user can possess simultaneously.

Specify absolute limits to limit the overall number of items or amount of capacity in the system. 
Absolute limits also include the amount of resources currently consumed, which allow for programmatic visibility of usage.

Rate limits
-----------
Rate limits control the frequency at which 
the user can issue specific requests. 
Rate limits are reset after a certain amount of time passes. 
To request a rate limit increase, contact Rackspace.

Limits for specific services
----------------------------
This table shows some examples of limits, 
with links to API documentation for 
more examples and complete details.

+--------------------+-----------------------+--------------------+
|Service             |Absolute limit example |Rate limit example  |
|                    | + link for details    | + link for details |          
+=====================+======================+====================+
|Cloud Block Storage |10 TB                  |no limits           | 
|                    |see API doc            |                    |
+--------------------+-----------------------+--------------------+
|Cloud Servers       |100 servers in config  |xxxxxxxxx           | 
|                    |see API doc            |                    |
+--------------------+-----------------------+--------------------+
|Cloud Images        |no limits              |no limits           | 
|                    |                       |                    |
+--------------------+-----------------------+---=----------------+
|Cloud Networks      |no limits              |no limits           | 
|                    |                       |                    |
+--------------------+-----------------------+--------------------+

.. NOTE::
   The services discussed here are not the only ones 
   with absolute limits or rate limits.
   Some services have no limits. 
   We publish the limits relevant to any service 
   in that service's 
   API documentation. You can find those details
   by going to http://docs.rackspace.com/
   and searching for "limits". 
