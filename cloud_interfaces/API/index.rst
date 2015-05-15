.. _cloud_interfaces_API:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
API & SDK: Developer and DevOps tools
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If you write applications that are tightly integrated with 
the Rackspace cloud 
you may find that the Control Panel and CLIs are not ideal for
your purposes. 
If you develop or distribute applications for your customers, 
or if you wish to heavily automate operation of your 
cloud infrastructure,
you may need to interact with cloud services 
through one of the many available Software Development Kits 
or by 
direct API access

Software Development Kits (SDKs)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Software development kits provide
easy to use, language-specific interfaces 
for accessing and integrating
APIs into your applications and workflows. 
Often these libraries also
abstract the functionality required to support your applications and
workloads across multiple cloud endpoints or providers.

Rackspace supports SDKs for the following languages:

* Go

* Java

* .Net

* Node.js

* PHP

* Python

* Ruby

You can find links to all the Rackspace-supported SDKs, with
installation instructions, guidance, tutorials, and more for each, at
https://developer.rackspace.com/sdks/.

Direct API access
^^^^^^^^^^^^^^^^^
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
We have documented basic
functions for many APIs in many popular programming languages in
quickstart guides for developers at
https://developer.rackspace.com/docs/. However, knowing the API
structure and being able to make direct, manual calls to the API is a
powerful tool for understanding and managing the Rackspace Cloud
infrastructure.

The API Developer Guide for each service is available at
http://docs.rackspace.com/; the same API operations are also listed
in a 
combined reference at http://api.rackspace.com/.

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
 
We published these API documents primarily to support readers who are 
already experienced with RESTful APIs in other contexts and 
are seeking details specifically about Rackspace's APIs. 
We don't publish a beginner-level API tutorial. 
However, REST is widely used and introductory material is
readily available. 
If you wish to work with our APIs and this would be your first
experience with RESTful APIs, 
begin with :ref:`setup_API`.


DevOps tools
^^^^^^^^^^^^
If you use popular DevOps tools such as Knife, Vagrant, Ansible, and
Salt, you may be interested in plugins (official or unofficial) for
these automation frameworks. Sources of more information about these
plugins include:

* Knife: https://github.com/opscode/knife-rackspace

* Vagrant: https://github.com/mitchellh/vagrant-rackspace

* Ansible: http://docs.ansible.com/guide_rax.html

* Salt: http://docs.saltstack.com/en/latest/topics/cloud/rackspace.html

Contents:

.. toctree::
   :maxdepth: 2

   setup_API
   cloudservers_API
   cloudnetworks_API
   cloudimages_API
   cloudblockstorage_API
   moreinfo_API
