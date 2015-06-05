.. _cloudimages_API:

------------------------------
Cloud Images and SDKs and APIs
------------------------------
When you begin writing your own software
to interact with Cloud Images, 
you may benefit from investing some time to learn about 
how Cloud Images works
in the Cloud Control Panel 
and how SDKs and APIs are documented at Rackspace.

.. _cloudimages_APIinvestigation:

++++++++++++++++++++++++++++++
Cloud Images API investigation
++++++++++++++++++++++++++++++
Using an API, 
you can write software to automate functions that could otherwise 
be performed manually by a person logged into the Cloud Control Panel. 
You can accelerate your understanding of how the API works 
by using the Cloud Control Panel to demonstrate the manual process 
before you begin to automate it; 
to interact with the Cloud Images service, 
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

.. _cloudimages_APIdemonstration:

++++++++++++++++++++++++++++++
Cloud Images API demonstration
++++++++++++++++++++++++++++++
Using the process suggested at 
:ref:`cloudimages_APIinvestigation`, 
here is an example of how you can plan 
and then write your own software to perform one simple task: 
list all your Cloud Images. 

Learn about Cloud Images in the Cloud Control Panel  
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the 
`Cloud Control Panel <https://mycloud.rackspace.com/>`__, 
your session begins with information about your Cloud Servers.
To see your Cloud Images information, click ``Servers`` 
and then click ``Saved Images``. 

.. figure:: /_images/ServersSavedImages.png
   :scale: 80%
   :alt: To move from Cloud Servers to 
         Cloud Images details, 
         click Servers and then click Saved Images.
   
   To move from Cloud Servers to 
   Cloud Images details, 
   click Servers and then click Saved Images.
     
By default, the list is focused on your account's home region, 
showing all images in that region; 
you can select a different region and you can search for a 
specific image.

If your list of images is not empty, then for each image 
you can see 

* its name
* the server from which it was created
* its creation date
* its size

.. figure:: /_images/CloudImagesListAll.png
   :alt: The Cloud Control Panel lists all of your
         Cloud Networks networks.
         
   The Cloud Control Panel lists all of your
   Cloud Networks networks.
         
.. include:: note-chrome-devtools.rst

Learn about Cloud Images in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the 
`API cross-reference <http://api.rackspace.com/>`__,
you can see all available API operations for all cloud services. 
The operations are grouped according to the service they interact 
with (for example, Cloud Images or Cloud Files) 
and the scope they act upon (for example, images or image schemas). 

You can see all Cloud Images operations in the 
`API cross-reference <http://api.rackspace.com/api-ref-images.html>`__; 
in the group of 
`operations that act upon images <http://api.rackspace.com/api-ref-images.html#images>`__, 
you can see that:
   
* sending a ``GET`` to the ``images``  
  URI requests a basic list of information about public images

* sending a ``GET`` to the same URI and appending an image ID 
  requests an expanded list of information about a single image

.. figure:: /_images/CloudImagesListImagesGET.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations.
   
   The API cross-reference lists all API operations.

On the first ``GET`` line, click *detail* to see 
more about how the API handles this request.  
The request parameters and sample response shown here can 
help you formulate a basic *List images* request to the API 
and understand the API's 
response.

In the sample response, 
``name``, ``created_at``, ``size``, and ``id`` 
correspond to the information available on the Cloud Control Panel.

In the 
`Getting Started Guide for the Cloud Images API <http://docs.rackspace.com/images/api/v2/ci-gettingstarted/>`__, 
you can see an example of  
`obtaining a list of images by using the cURL command-line interface (CLI) 
<http://docs.rackspace.com/images/api/v2/ci-gettingstarted/content/list-images.html>`__. 

Learn about Cloud Images in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the 
`SDK QuickStart for Cloud Images <https://developer.rackspace.com/docs/cloud-images/getting-started/>`__,
you can see some of the same steps that are documented in 
the API's Getting Started Guide. 
For example, both the API-focused and SDK-focused documents 
show how to authenticate with your API key before issuing any requests 
to the Cloud Images API.

The SDK QuickStart adds examples in several popular programming 
languages, 
demonstrating how to use each language to 
code some commonly-used requests to the 
Cloud Images API.

To see examples in a specific language, 
click that language's name in the list across the top of the page. 
For example, to see Cloud Images code samples coded in python, 
go to the 
`SDK QuickStart for Cloud Images <https://developer.rackspace.com/docs/cloud-images/getting-started/>`__ 
and click *python*.

.. figure:: /_images/CloudImagesSDKpython.png
   :scale: 80%
   :alt: Python is one of several languages for which we 
         publish an SDK QuickStart.
         
   Python is one of several languages for which we 
   publish an SDK QuickStart.

Use SDK to help you write and run code to interact with Cloud Images
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests; 
for more detailed guidance, 
perhaps enough to walk you through exactly the steps required 
to develop your software, examine the SDK itself. 

To find the full SDK for your programming language, start at 
`SDKs & Tools in the Developer Center <https://developer.rackspace.com/sdks/>`__ 
and find the language. 
Then follow the steps appropriate to that language.

For example, if you code in python, 

* Follow the installation instructions to give yourself 
  a local copy of the pyrax (python for Rackspace) SDK. 
* Click *documentation* to open the 
  `GitHub repository for the pyrax SDK <https://github.com/rackspace/pyrax/>`__. 
* In that pyrax repository, at 
  `/docs/ <https://github.com/rackspace/pyrax/tree/master/docs>`__,
  you can see documents specific to 
  three of the four core infrastructure services: 
  Cloud Servers, Cloud Networks, Cloud Block Storage. 
  Although no document is specific to Cloud Images, 
  you can adapt the examples in one of the others.  
