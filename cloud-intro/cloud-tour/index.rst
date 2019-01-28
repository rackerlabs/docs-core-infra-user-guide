.. _cloud-tour:

-----------------------------------------------
Touring the Rackspace cloud, service by service
-----------------------------------------------
Rackspace's managed cloud is more than a virtualized representation
of physical
computing resources, but thinking of it that way may help you
understand
how so many different services combine to support your workload.

Just as
if you had a fixed configuration of physical computing equipment, the
services that provide you with flexible computing in the cloud must
perform essential tasks:

* Deliver processing power
  (Cloud Servers)
* Connect servers in an internal network
  (Cloud Networks)
* Quickstart new servers according to predefined patterns
  (Cloud Images)
* Expand storage attached to one server and transferable to others
  (Cloud Block Storage)
* Long-term storage for unlimited objects (Cloud Files)

We consider
these five services to be the core infrastructure of our managed cloud;
the core infrastructure is the focus of this guide.

Beyond the cloud's core infrastructure,
other services provide additional functions.
Depending on your workload, you may need to use some or
all of these:

* Authentication (Identity)
* Data services (Cloud Databases, Cloud Big Data, Object Rocket)
* Recoverability (Cloud Backup)
* Distribution of public-facing content (Rackspace CDN)
* Connections to public-facing networks
  (Cloud DNS, Cloud Load Balancers)
* Connections to dedicated hardware (RackConnect)
* Automated installation (Cloud Orchestration)
* Automated reconfiguration (Auto Scale)
* Observation of activity
  (Cloud Monitoring, Cloud Metrics, Cloud Feeds)

These services work well with the core infrastructure and with
each other. They are not the primary focus of this guide, but we'll
mention them when they are relevant.

In other Rackspace resources such as the
`Cloud Control Panel <https://mycloud.rackspace.com/>`__
and
`technical documentation <http://www.rackspace.com/knowledge_center/>`__,
you should notice that Rackspace cloud products
are grouped so that closely-related products are likely to be discussed together.
We follow that convention here, introducing several categories of cloud products
available as services in the Rackspace cloud:

* :ref:`tour-compute-services`
* :ref:`tour-network-services`
* :ref:`tour-storage-services`
* :ref:`tour-data-services`
* :ref:`tour-application-services`
* :ref:`tour-support-services`



.. toctree::
   :maxdepth: 2

   compute-services
   network-services
   storage-services
   data-services
   application-services
   support-services
