.. _cloudblockstorage_API:

-------------------------------------
Cloud Block Storage and SDKs and APIs
-------------------------------------
When you begin writing your own software
to interact with Cloud Block Storage, 
you may benefit from investing some time to learn about 
how Block Storage works
in the Cloud Control Panel 
and how SDKs and APIs are documented at Rackspace.

.. _cloudblockstorage_APIinvestigation:

+++++++++++++++++++++++++++++++++++++
Cloud Block Storage API investigation
+++++++++++++++++++++++++++++++++++++
Using an API, 
you can write software to automate functions that could otherwise 
be performed manually by a person logged into the Cloud Control Panel. 
You can accelerate your understanding of how the API works 
by using the Cloud Control Panel to demonstrate the manual process 
before you begin to automate it; 
to interact with the Cloud Block Storage service, 
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

.. _cloudblockstorage_APIdemonstration:

+++++++++++++++++++++++++++++++++++++
Cloud Block Storage API demonstration
+++++++++++++++++++++++++++++++++++++
Using the process suggested at 
:ref:`cloudblockstorage_APIinvestigation`, 
here is an example of how you can plan 
and then write your own software to perform one simple task: 
list all your Cloud Block Storage volumes. 

Learn about Cloud Block Storage in the Cloud Control Panel  
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the 
`Cloud Control Panel <https://mycloud.rackspace.com/>`__, 
your session begins with information about your Cloud Servers.
To see your Cloud Block Storage information, click ``Storage`` 
and then click ``Block Storage Volumes``. 

.. figure:: /_images/StorageBlockStorageVolumes.png
   :scale: 80%
   :alt: To move from Cloud Servers to 
         Cloud Block Storage details, 
         click Storage and then click Block Storage Volumes.

   To move from Cloud Servers to 
   Cloud Block Storage details, 
   click Storage and then click Block Storage Volumes.

By default, the list is focused on your account's home region, 
showing all volumes in that region; 
you can select a different region and you can search for a 
specific volume.

.. figure:: /_images/CloudBlockStorage0volumes.png
   :scale: 80%
   :alt: If you have no Cloud Block Storage volumes, 
         the Cloud Control Panel shows you how to 
         create one.
         
   If you have no Cloud Block Storage volumes, 
   the Cloud Control Panel shows you how to 
   create one.
         
If your list of volumes is not empty, then for each volume 
you can see: 

* its ID
* the name of the server to which it is attached
* the region in which it is located
* the type of disk it uses
* its size

.. figure:: /_images/CloudBlockStorage1volume.png
   :scale: 80%
   :alt: The Cloud Control Panel lists all of your
         Cloud Block Storage volumes.
         
   The Cloud Control Panel lists all of your
   Cloud Block Storage volumes.
         
.. include:: note-chrome-devtools.rst

Learn about Cloud Block Storage in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the 
`API cross-reference <http://api.rackspace.com/>`__, 
you can see all available API operations for all cloud services. 
The operations are grouped according to the service they interact 
with (for example, Cloud Block Storage or Cloud Files) 
and the scope they act upon (for example, volumes or snapshots). 

You can see all Cloud Block Storage operations in the 
`API cross-reference <http://api.rackspace.com/api-ref-blockstorage.html>`__; 
in the group of 
`operations that act upon volumes <http://api.rackspace.com/api-ref-blockstorage.html#volumes>`__, 
you can see that:

* sending a ``POST`` to the ``v1/{tenant_id}/volumes`` 
  URI requests creation of a new server

* sending a ``GET`` to the same URI  
  requests a basic list of information about volumes

* sending a ``GET`` to the same URI and appending ``/detail`` 
  requests an expanded list of information about volumes

.. figure:: /_images/CloudBlockStorageListVolumesGET.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations.
   
   The API cross-reference lists all API operations.

On the first ``GET`` line, click *detail* to see 
more about how the API handles this request.  
The request parameters and sample response shown here can 
help you formulate a basic *List volumes* request to the API 
and understand the API's 
response. 
  
In the sample response, 
``id``, ``display_name``, ``size``, and ``volume_type`` 
correspond to the information available on the Cloud Control Panel. 
 
In the 
`Getting Started Guide for the Cloud Block Storage API <http://docs.rackspace.com/cbs/api/v1.0/cbs-getting-started/>`__, 
you can see an example of  
`obtaining a list of Cloud Block Storage volumes by using the cURL command-line interface (CLI) 
<http://docs.rackspace.com/cbs/api/v1.0/cbs-getting-started/content/Listing_volumes_d1e060.html>`__. 

Learn about Cloud Block Storage in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the 
`SDK QuickStart for Cloud Block Storage <https://developer.rackspace.com/docs/cloud-block-storage/getting-started/>`__,
you can see some of the same steps that are documented in 
the API's Getting Started Guide. 
For example, both the API-focused and SDK-focused documents 
show how to authenticate with your API key before issuing any requests 
to the Cloud Block Storage API. 
 
The SDK QuickStart adds examples in several popular programming 
languages, 
demonstrating how to use each language to 
code some commonly-used requests to the 
Cloud Block Storage API. 

To see examples in a specific language, 
click that language's name in the list across the top of the page. 
For example, to see Cloud Block Storage code samples coded in PHP, 
go to the 
`SDK QuickStart for Cloud Block Storage <https://developer.rackspace.com/docs/cloud-block-storage/getting-started/>`__ 
and click *PHP*. 

.. figure:: /_images/CloudBlockStorageSDKPHP.png
   :scale: 80%
   :alt: PHP is one of several languages for which we 
         publish an SDK QuickStart.
         
   PHP is one of several languages for which we 
   publish an SDK QuickStart.

Use SDK to help you write and run code to interact with Cloud Block Storage
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests; 
for more detailed guidance, 
perhaps enough to walk you through exactly the steps required 
to develop your software, examine the SDK itself. 

To find the full SDK for your programming language, start at 
`SDKs & Tools in the Developer Center <https://developer.rackspace.com/sdks/>`__ 
and find the language. 
Then follow the steps appropriate to that language. 

For example, if you code in PHP, 

* Follow the installation instructions to give yourself 
  a local copy of the php-opencloud SDK. 
* In the 
  `documentation repository for php-opencloud <http://docs.php-opencloud.com/>`__,
  read about the *Volumes v1* service, 
  applicable to both Rackspace and OpenStack configurations. 
  In that document,  
  you can go directly to an 
  `example of listing Cloud Block Storage volumes <http://docs.php-opencloud.com/en/latest/services/volume/volumes.html#list-volumes>`__. 
