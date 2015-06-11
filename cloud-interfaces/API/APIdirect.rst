.. _APIdirect:

-----------------
Direct API access
-----------------
Each of our cloud services exposes an API which can be leveraged for
low-level integration with the service. 
Rackspace APIs, 
like OpenStack APIs, 
are Representational State Transfer (REST) APIs, 
meaning they are is logically
structured, stateless, and scalable (among other properties). 

For most use cases, we recommend 
working with the guidance of an SDK
rather than integrating directly with an API. 
In the 
`Developer Center <https://developer.rackspace.com/docs/>`__, 
we have documented basic 
functions for many APIs in many popular programming languages in
quickstart guides. However, knowing the API
structure and being able to make direct, manual calls to the API is a
powerful tool for understanding and managing the Rackspace Cloud
infrastructure.

The API Developer Guide for each service is published in 
`our technical documentation collection <http://docs.rackspace.com/>`__; 
the same API operations are also listed 
in a 
combined 
`API cross-reference <http://api.rackspace.com/>`__.

Some of the most common ways to directly interact with APIs are:

* command line tools, 
  such as 
  `cURL <http://curl.haxx.se/>`__

* browser extensions, 
  such as 
  `Postman for Chrome <https://www.getpostman.com/>`__

* utilities for specific operating systems,  
  such as those listed in your app store or directory 
  under *REST client*

For each service that offers a public API, 
Rackspace publishes at least two technical documents:
 
* `API Developer Guide <http://docs.rackspace.com>`__: 
  reference material *describing* API requests and sample responses
   
* `API Getting Started Guide <http://docs.rackspace.com>`__: 
  tutorial material *demonstrating* simple interactions
  with the API 
  
For most APIs, we also publish 
`API Release Notes <http://docs.rackspace.com>`__, 
*announcing* changes to the API. 
 
We publish these API documents primarily to support readers who are 
already experienced with RESTful APIs in other contexts and 
are seeking details specifically about Rackspace's APIs. 
We don't publish a beginner-level API tutorial. 
However, REST is widely used and introductory material is
readily available. 
If you wish to work with our APIs and this would be your first
experience with RESTful APIs, 
begin with :ref:`setup_API`.
