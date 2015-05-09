.. _cloudimages_API:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Images and SDKs and APIs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
When you begin writing your own software
to interact with Cloud Images, 
you may benefit from investing some time to learn about 
how Cloud Images works
in the Cloud Control Panel 
and how SDKs and APIs are documented at Rackspace.

.. _cloudimages_APIinvestigation:

------------------------------
Cloud Images API investigation
------------------------------
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
API documentation, http://docs.rackspace.com. 

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

------------------------------
Cloud Images API demonstration
------------------------------
Using the process suggested at 
:ref:`cloudimages_APIinvestigation`, 
here is an example of how you can plan 
and then write your own software to perform one simple task: 
list all your Cloud Images. 

When you login to the 
`Cloud Control Panel <https://mycloud.rackspace.com/>`__, 
your session begins with information about your Cloud Servers.
To see your Cloud Images information, click ``Servers`` 
and then click ``Saved Images``. 

.. image:: ../../screenshots/ServersSavedImages.png
   :alt: To move from Cloud Servers to 
         Cloud Images details, 
         click Servers and then Saved Images.
         
xxxxxxxx