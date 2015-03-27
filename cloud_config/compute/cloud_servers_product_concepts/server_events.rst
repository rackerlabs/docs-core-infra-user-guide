.. _server_events:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Monitoring events on your Cloud Server
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Automated monitoring of your Cloud Server configuration and its entire
infrastructure stack enables you to know how your system is being used
and respond to changes quickly and flexibly.

Monitoring operates on two levels:

* remote monitoring, managed by Rackspace and based in our global data
  centers

* agent-based monitoring, available for you to configure on your Cloud
  Servers

Cloud Monitoring is included at no charge with every cloud account.

You can customize your monitoring configuration in several ways:

* choose which servers to monitor 
  (for example, you may not wish to be bothered when
  a test-only system fails)

* choose which regions to monitor 
  (for example, you may be particularly concerned
  about a new project based in HKG)

* describe what kind of activity or inactivity is cause for alarm 
  (for example, you
  may wish to know when a monitored resource takes longer than 50
  milliseconds to respond to a ping)

* identify whom to notify and how to notify them    
  (for example, you may wish to send
  email to your DevOps team list when a resource reaches a warning
  state, then a pager message to your Customer Support team when the
  resource reaches a failed state)

Because Rackspace Cloud Monitoring is closely integrated with Rackspace
Auto Scale, your monitoring configuration can become the basis of your
autoscaling configuration. Used in combination, Cloud Monitoring can
report an event (for example, a workload spike on a Cloud Server) and
Auto Scale can respond to that report (for example, by adding a Cloud
Server to share the workload within a Cloud Load Balancer group).

You can interact with Cloud Monitoring and Auto Scale using the same
methods you use to interact with Cloud Servers:

* the `Cloud Control Panel <https://mycloud.rackspace.com/>`__, as
  explained in the `Knowledge
  Center <http://www.rackspace.com/knowledge_center/>`__

* the raxmon Command Line Interface

* `Software Development Kits <https://developer.rackspace.com/>`__

* `Application Programming Interfaces <http://docs.rackspace.com/>`__
