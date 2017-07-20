.. _cloudnetworks-api:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Networks and SDKs and APIs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you begin writing your own software
to interact with Cloud Networks,
you might want to learn about
how Cloud Networks works
in the Cloud Control Panel
and how SDKs and APIs are documented at Rackspace.

.. _cloudnetworks-api-investigation:

++++++++++++++++++++++++++++++++
Cloud Networks API investigation
++++++++++++++++++++++++++++++++
Using an API,
you can write software to automate functions that could otherwise
be performed manually by a person logged in to the Cloud Control Panel.
You can accelerate your understanding of how the API works
by using the Cloud Control Panel to demonstrate the manual process
before you begin to automate it;
to interact with the Cloud Networks service,
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

.. _cloudnetworks-api-demonstration:

++++++++++++++++++++++++++++++++
Cloud Networks API demonstration
++++++++++++++++++++++++++++++++
Using the process suggested at
:ref:`cloudnetworks-api-investigation`,
this section provides an example of how you can plan
and then write your own software to perform one simple task:
list all your cloud networks.

Learn about Cloud Networks in the Cloud Control Panel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the
:mycloud:`Cloud Control Panel <>`,
your session begins with information about your servers.
To see your Cloud Networks information, click **Networking**
and then click **Networks**.

.. figure:: /_images/networkingnetworks.png
   :scale: 80%
   :alt: To move from Cloud Servers to
         Cloud Networks details,
         click Networking and then Networks.

   *To move from Cloud Servers to
   Cloud Networks details,
   click "Networking" and then click "Networks".*

By default, the list is focused on your account's home region,
showing all networks in that region;
you can select a different region and you can search for a
specific network.

If your list of networks is not empty, then for each network
you can see

* Its name
* Its IP address in CIDR format
* The region in which it is located

.. figure:: /_images/cloudnetworkslistall.png
   :scale: 80%
   :alt: The Cloud Control Panel lists all of your
         Cloud Networks networks.

   *The Cloud Control Panel lists all of your
   Cloud Networks networks.*

.. include:: /_common/note-chrome-devtools.txt

Learn about Cloud Networks in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the
:rax-api:`API cross-reference <>`,
you can see all available API operations for all cloud services.
The operations are grouped according to the service they interact
with (for example, Cloud Networks or Cloud Files)
and the scope they act on (for example, subnets or ports).

You can see all Cloud Networks operations in the
:rax-docs:`Cloud Networks API Reference <cloud-networks/v2/api-reference/>`.
In the group of
:rax-docs:`Network operations <cloud-networks/v2/api-reference/network-operations>`,
you can see that:

* Sending a ``GET`` request to the ``v2.0/networks``
  URI requests a basic list of information about networks

* Sending a ``POST`` request to the same
  URI requests creation of a new network

* Sending a ``GET`` request to the same URI and appending a network ID
  requests an expanded list of information about a single network

.. figure:: /_images/cloudnetworkslistnetworksget.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations.

   *The API cross-reference lists all API operations. Click "detail" to
   see more about how the API handles this request.*

The request parameters and sample response shown here can
help you formulate a basic *List networks* request to the API
and understand the API's response.

In the sample response,
``name`` and ``id``
correspond to the information available on the Cloud Control Panel.

In the
:rax-docs:`Getting Started Guide for the Cloud Networks API <cloud-networks/v2/getting-started/>`,
you can see an example of
:rax-docs:`obtaining a list of networks by using the cURL command-line interface (CLI)
<cloud-networks/v2/getting-started/managing-networks/creating-network-curl/#listing-networks-curl>`.

Learn about Cloud Networks in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the
:rax-dev-quickstart:`SDK QuickStart for Cloud Networks <cloud-networks/getting-started>`,
you can see some of the same steps that are documented in  the API's Getting
Started Guide. For example, both the API-focused and SDK-focused documents
show how to authenticate with your API key before issuing any requests to the
Cloud Networks API.

The SDK QuickStart adds examples in several popular programming
languages,
demonstrating how to use each language to
code some commonly-used requests to the
Cloud Networks API.

To see examples in a specific language,
click that language's name in the list across the top of the page.
For example, to see Cloud Networks code samples coded in Java,
go to the
:rax-dev-quickstart:`SDK QuickStart for Cloud Networks <cloud-networks/getting-started>`
and click *Java*.

.. figure:: /_images/cloudnetworkssdkjava.png
   :scale: 80%
   :alt: Java is one of several languages for which we
         publish an SDK QuickStart.

   *Java is one of several languages for which we
   publish an SDK QuickStart.*

Use SDK to help you write and run code to interact with Cloud Networks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests;
for more detailed guidance that will help you
develop your software, examine the SDK itself.

To find the full SDK for your programming language, start at
:rax-dev:`SDKs & Tools in the Developer Center <sdks>`
and find the language.

For example, if you code in Java,

* Follow the installation instructions to give yourself
  a local copy of the Apache jclouds SDK.
* In the
  `GitHub repository for jclouds <https://github.com/jclouds/jclouds-examples/tree/master/rackspace/src/main/java/org/jclouds/examples/rackspace/cloudnetworks>`__,
  examine the examples of Cloud Networks code.
  No complete example of a *List networks* request is provided,
  but you can use the other examples as guides to help you
  adapt the partial *List networks* request in the
  :rax-dev-quickstart:`SDK QuickStart <cloud-networks/getting-started/#list-networks>`.
