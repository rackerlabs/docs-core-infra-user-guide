.. _cloudnetworks_API:

--------------------------------
Cloud Networks and SDKs and APIs
--------------------------------
When you begin writing your own software
to interact with Cloud Networks, 
you may benefit from investing some time to learn about 
how Cloud Networks works
in the Cloud Control Panel 
and how SDKs and APIs are documented at Rackspace.

.. _cloudnetworks_APIinvestigation:

++++++++++++++++++++++++++++++++
Cloud Networks API investigation
++++++++++++++++++++++++++++++++
Using an API, 
you can write software to automate functions that could otherwise 
be performed manually by a person logged into the Cloud Control Panel. 
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
via the API 
that could not be performed in any other way; 
product announcements for Limited Availability 
and Early Access releases point out this limitation when it applies. 
In that case, 
experimenting in the Cloud Control Panel can show you 
only part of the process of working with a new feature; 
other details are described in the 
`API documentation <http://docs.rackspace.com>`__. 

Just as you can use the Cloud Control Panel 
to help you understand a manual process that you intend to automate, 
you can use the API documentation to help you understand 
how to use a Software Development Kit (SDK) 
in your favorite programming language. 

* The API documentation describes 
  *what* you can ask the API to do. 
  
* The SDK documentation demonstrates 
  *how* to ask the API to do something. 

Awareness of both API and SDK capabilities 
can help you to plan the easiest way to develop your software.

.. _cloudnetworks_APIdemonstration:

++++++++++++++++++++++++++++++++
Cloud Networks API demonstration
++++++++++++++++++++++++++++++++
Using the process suggested at 
:ref:`cloudnetworks_APIinvestigation`, 
here is an example of how you can plan 
and then write your own software to perform one simple task: 
list all your Cloud Networks. 

Learn about Cloud Networks in the Cloud Control Panel  
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the 
`Cloud Control Panel <https://mycloud.rackspace.com/>`__, 
your session begins with information about your Cloud Servers.
To see your Cloud Networks information, click ``Networking`` 
and then click ``Networks``. 

.. figure:: /_images/NetworkingNetworks.png
   :scale: 80%
   :alt: To move from Cloud Servers to 
         Cloud Networks details, 
         click Networking and then Networks.
         
   To move from Cloud Servers to 
   Cloud Networks details, 
   click Networking and then click Networks.
         
By default, the list is focused on your account's home region, 
showing all networks in that region; 
you can select a different region and you can search for a 
specific network.

If your list of networks is not empty, then for each network 
you can see 

* its name
* its IP address in CIDR format
* the region in which it is located

.. figure:: /_images/CloudNetworksListAll.png
   :scale: 80%
   :alt: The Cloud Control Panel lists all of your
         Cloud Networks networks.  
         
   The Cloud Control Panel lists all of your
   Cloud Networks networks.  
                  
.. include:: note-chrome-devtools.rst

Learn about Cloud Networks in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the 
`API cross-reference <http://api.rackspace.com/>`__, 
you can see all available API operations for all cloud services. 
The operations are grouped according to the service they interact 
with (for example, Cloud Networks or Cloud Files) 
and the scope they act upon (for example, subnets or ports). 

You can see all Cloud Networks operations in the 
`API cross-reference <http://api.rackspace.com/api-ref-networks.html>`__; 
in the group of 
`operations that act upon networks <http://api.rackspace.com/api-ref-networks.html#network-ops>`__, 
you can see that:

* sending a ``GET`` to the ``v2.0/networks``  
  URI requests a basic list of information about networks

* sending a ``POST`` to the same 
  URI requests creation of a new network

* sending a ``GET`` to the same URI and appending a network ID 
  requests an expanded list of information about a single network

.. figure:: /_images/CloudNetworksListNetworksGET.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations.
   
   The API cross-reference lists all API operations.

On the first ``GET`` line, click *detail* to see 
more about how the API handles this request.  
The request parameters and sample response shown here can 
help you formulate a basic *List networks* request to the API 
and understand the API's 
response.

In the sample response, 
``name`` and ``id`` 
correspond to the information available on the Cloud Control Panel. 

In the 
`Getting Started Guide for the Cloud Networks API <http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/>`__, 
you can see an example of  
`obtaining a list of networks by using the cURL command-line interface (CLI) 
<http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/neutron_list_networks_curl.html>`__. 

Learn about Cloud Networks in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the 
`SDK QuickStart for Cloud Networks <https://developer.rackspace.com/docs/cloud-networks/getting-started/>`__,
you can see some of the same steps that are documented in 
the API's Getting Started Guide. 
For example, both the API-focused and SDK-focused documents 
show how to authenticate with your API key before issuing any requests 
to the Cloud Networks API. 
 
The SDK QuickStart adds examples in several popular programming 
languages, 
demonstrating how to use each language to 
code some commonly-used requests to the 
Cloud Networks API.

To see examples in a specific language, 
click that language's name in the list across the top of the page. 
For example, to see Cloud Networks code samples coded in Java, 
go to the 
`SDK QuickStart for Cloud Networks <https://developer.rackspace.com/docs/cloud-networks/getting-started/>`__ 
and click *Java*. 

.. figure:: /_images/CloudNetworksSDKjava.png
   :scale: 80%
   :alt: Java is one of several languages for which we 
         publish an SDK QuickStart.
         
   Java is one of several languages for which we 
   publish an SDK QuickStart.
         
Use SDK to help you write and run code to interact with Cloud Networks
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests; 
for more detailed guidance, 
perhaps enough to walk you through exactly the steps required 
to develop your software, examine the SDK itself. 

To find the full SDK for your programming language, start at 
`SDKs & Tools in the Developer Center <https://developer.rackspace.com/sdks/>`__ 
and find the language. 
Then follow the steps appropriate to that language. 

For example, if you code in Java, 

* Follow the installation instructions to give yourself 
  a local copy of the Apache jclouds SDK. 
* In the 
  `GitHub repository for jclouds <https://github.com/jclouds/jclouds-examples/tree/master/rackspace/src/main/java/org/jclouds/examples/rackspace/cloudnetworks>`__,
  examine the examples of Cloud Networks code. 
  No complete example of a *List networks* request is provided, 
  but you can use the other examples as guides to help you
  adapt the partial *List networks* request in the 
  `SDK QuickStart <https://developer.rackspace.com/docs/cloud-networks/getting-started/#list-networks>`__.
