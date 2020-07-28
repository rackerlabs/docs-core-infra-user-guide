.. _cloudservers-api:

^^^^^^^^^^^^^^^^^^^^^^
Cloud Servers and APIs
^^^^^^^^^^^^^^^^^^^^^^
When you begin writing your own software
to interact with Cloud Servers,
you might want to learn about
how Cloud Servers works
in the Cloud Control Panel
and how SDKs and APIs are documented at Rackspace.

.. _cloudservers-api-investigation:

+++++++++++++++++++++++++++++++
Cloud Servers API investigation
+++++++++++++++++++++++++++++++
Using an API,
you can write software to automate functions that could otherwise
be performed manually by a person logged in to the Cloud Control Panel.
You can accelerate your understanding of how the API works
by using the Cloud Control Panel to demonstrate the manual process
before you begin to automate it;
to interact with the Cloud Servers service,
the Cloud Control Panel sends requests via the same API
that you interact with when you write your own software.

Sometimes,
especially for new features that are not yet available
in the Cloud Control Panel,
you can write software to perform functions
using the API
that could not be performed in any other way.
Product announcements for Limited Availability
and Early Access releases point out this limitation when it applies.
In that case,
experimenting in the Cloud Control Panel can show you
only part of the process of working with a new feature;
other details are described in the
:rax-docs:`API documentation <>`.

Just as you can use the Cloud Control Panel
to help you understand a manual process that you intend to automate,
you can use the API documentation to help you understand
how to use API operations to automate cloud functions.

The API documentation describes what you can accomplish, how to structure an 
API operation, and what responses to expect.

After you understand what the Cloud Servers API is capable of,
investigate whether the automation you require is already available from 
another Rackspace product or from a Rackspace partner.

For example:

* :rax-cloud:`Auto Scale <auto-scale>`
  responds to workload peaks by increasing server capacity.

* :rax-cloud:`Cloud Orchestration <orchestration>`
  installs a complete application stack on a server.

* :rax-cloud:`Cloud Backup <backup>`
  automates a server's backup schedule.

Good places to investigate relevant capabilities
available within the broader Rackspace portfolio include:

* Rackspace product summaries such as
  :rax-cloud:`Rackspace Cloud Servers powered by OpenStack <servers>`
* :how-to:`Rackspace technical documentation <>`

.. _cloudservers-api-demonstration:

+++++++++++++++++++++++++++++++
Cloud Servers API demonstration
+++++++++++++++++++++++++++++++
Using the process suggested at
:ref:`cloudservers-api-investigation`,
this section provides an example of how you can plan
and then write your own software to perform one simple task:
list all your cloud servers.

Learn about Cloud Servers in the Cloud Control Panel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the
:mycloud:`Cloud Control Panel <>`,
your session begins with a list of all your servers.
By default, the list is unfiltered,
showing every server;
you can narrow the list by clicking on filters
for tag, status, image, flavor, and type.

.. figure:: /_images/cloudserverslistall.png
   :scale: 80%
   :alt: The Cloud Control Panel lists all of your
         Cloud Servers.

   *The Cloud Control Panel lists all of your
   Cloud Servers.*

.. include:: /_common/note-chrome-devtools.txt

Learn about Cloud Servers in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the :rax-docs:`API documentation <>`,
you can see all available API operations for all cloud services.
The operations are grouped according to the service they interact
with (for example, Cloud Servers or Cloud Files)
and the scope they act on (for example, flavors or images).

You can see all Cloud Servers operations in the
:rax-docs:`Cloud Servers API Reference <cloud-servers/v2/api-reference/>`.
In the group of
:rax-docs:`Server operations <cloud-servers/v2/api-reference/svr-basic-operations/>`,
you can see that:

* Sending a ``GET`` request to the ``/v2/{tenant_id}/servers``
  URI requests a basic list of information about servers

* Sending a ``POST`` request to the same URI requests
  the creation of a new server

* Sending a ``GET`` request to the same URI and appending ``/detail``
  requests an expanded list of information about servers

The request parameters and sample response shown here can
help you formulate a basic *list servers* request to the API
and understand the API's response.

You can use request parameters to construct a request that returns
a list of only the Cloud Servers
that meet specific criteria.
In the sample response,
the request parameters named ``status``, ``image``, and ``flavor``
correspond to the filters available on the Cloud Control Panel.

In the
:rax-docs:`Getting Started Guide for Cloud Servers - Create your first server <cloud-servers/v2/getting-started/create-server-intro/>`,
you can follow a 3-step tutorial to perform an essential task:
create a cloud server.
The :rax-docs:`Getting Started Guide <cloud-servers/v2/getting-started/>`
begins with instructions on creating a Rackspace account
and walks you through basic server and network operations.
An intermediate step shows an example with the cURL command-line interface (CLI) for
:rax-docs:`Listing servers (cURL)
<cloud-servers/v2/getting-started/create-server/listing-servers-curl/>`.
