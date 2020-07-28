.. _cloudnetworks-api:

^^^^^^^^^^^^^^^^^^^^^^^
Cloud Networks and APIs
^^^^^^^^^^^^^^^^^^^^^^^
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
how to use API operations to automate cloud functions.

The API documentation describes what you can accomplish, how to structure an 
API operation, and what responses to expect.

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
In the :rax-docs:`API documentation <>`,
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

The request parameters and sample response shown here can
help you formulate a basic *List networks* request to the API
and understand the API's response.

In the sample response,
``name`` and ``id``
correspond to the information available on the Cloud Control Panel.

In the
:rax-docs:`Getting Started Guide for the Cloud Networks API <cloud-networks/v2/getting-started/>`,
you can see an example with the cURL command-line interface (CLI) for
:rax-docs:`Listing networks (cURL)
<cloud-networks/v2/getting-started/managing-networks/creating-network-curl/#listing-networks-curl>`.
