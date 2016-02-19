.. _cloudservers-api:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Servers and SDKs and APIs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
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
how to use a software development kit (SDK)
in your favorite programming language.

* The API documentation describes
  *what* you can ask the API to do.

* The SDK documentation demonstrates
  *how* to ask the API to do something.

Awareness of both API and SDK capabilities
can help you to plan the easiest way to develop your software.

After you understand what the Cloud Servers API is capable of
and how to use an SDK to simplify interaction with the API,
performing one more task may save you the effort of
writing your own software:
investigate whether the automation you require
is already available from another Rackspace product or from
a Rackspace partner.
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
* `Rackspace Community <https://community.rackspace.com/>`__
* `Rackspace Marketplace <https://marketplace.rackspace.com/listing?p=1&default=true&q#!/list/page/1/>`__
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
In the
:rax-api:`API cross-reference <>`,
you can see all available API operations for all cloud services.
The operations are grouped according to the service they interact
with (for example, Cloud Servers or Cloud Files)
and the scope they act on (for example, flavors or images).

You can see all Cloud Servers operations in the
:rax-api:`API cross-reference <api-ref.html#compute-core-v2>`.
In the group of
:rax-api:`operations that act on servers <api-ref.html#compute_servers>`
you can see that:

* Sending a ``GET`` request to the ``/v2/{tenant_id}/servers``
  URI requests a basic list of information about servers

* Sending a ``POST`` request to the same URI requests
  the creation of a new server

* Sending a ``GET`` request to the same URI and appending ``/detail``
  requests an expanded list of information about servers

.. figure:: /_images/cloudserverslistserversget.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations.

   *The API cross-reference lists all API operations Click "detail"
   to see more about how the API handles this request.*

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
:rax-docs:`Getting Started Guide for the Cloud Servers API <servers/api/v2/cs-gettingstarted>`,
you can follow a 12-step tutorial to perform an essential task:
create a cloud server.
The
:rax-docs:`tutorial <servers/api/v2/cs-gettingstarted/content/ch_gs_getting_started_with_nova.html>`
begins with instructions on creating a Rackspace account
and concludes with deleting the Cloud Server that was created.
An intermediate step
demonstrates
:rax-docs:`obtaining a detailed list of Cloud Servers by using the cURL command-line interface (CLI)
<servers/api/v2/cs-gettingstarted/content/curl_list_servers.html>`.

Learn about Cloud Servers in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the
:rax-dev-quickstart:`SDK QuickStart for Cloud Servers <cloud-servers/getting-started/>`,
you can see some of the same steps that are documented in
the API's Getting Started Guide.
For example, both the API-focused and SDK-focused documents
show how to authenticate with your API key before issuing any requests
to the Cloud Servers API.

The SDK QuickStart adds examples in several popular programming
languages,
demonstrating how to use each language to
code some commonly-used requests to the
Cloud Servers API.

To see examples in a specific language,
click that language's name in the list across the top of the page.
For example, to see Cloud Servers code samples coded in python,
go to the
:rax-dev-quickstart:`SDK QuickStart for Cloud Servers <cloud-servers/getting-started>`
and click **PYTHON**.

.. figure:: /_images/cloudserverssdkpython.png
   :scale: 80%
   :alt: Python is one of several languages for which we
         publish an SDK QuickStart.

   *Python is one of several languages for which we
   publish an SDK QuickStart.*

Use SDK to help you write and run code to interact with Cloud Servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests;
for more detailed guidance that will help you
develop your software, examine the SDK itself.

To find the full SDK for your programming language, start at
:rax-dev:`SDKs & Tools in the Develop Center <sdks>`
and find the language.

For example, if you code in python,

* Follow the installation instructions to give yourself
  a local copy of the pyrax (python for Rackspace) SDK.
* Click **documentation** to open the
  :rax-git:`GitHub repository for the pyrax SDK <pyrax/>`.
* In that pyrax repository, at
  :rax-git:`/docs/cloud_servers.md <pyrax/blob/master/docs/cloud_servers.md>`,
  read *Working with Cloud Servers*.
  That document begins with an
  :rax-git:`example of using pyrax to list servers <pyrax/blob/master/docs/cloud_servers.md#listing-servers>`.
