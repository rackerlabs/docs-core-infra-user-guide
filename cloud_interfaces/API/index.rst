.. _cloud_interfaces_API:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
API & SDK: Developer and DevOps tools
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
If you write applications that are tightly integrated with the Rackspace
Cloud you may find that the Control Panel and CLIs are not ideal for
your purposes. Those developing or distributing applications for their
customers, or doing heavy automation of their infrastructure on the
Rackspace Cloud, will often find it best to use either direct API access
or one of the many available Software Development Kits.

Software Development Kits (SDKs)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Software development kits take the powerful OpenStack APIs and provide
easy to use, language specific interfaces for accessing and integrating
them into your applications and workflows. Often these libraries also
abstract the functionality required to support your applications and
workloads across multiple cloud endpoints or providers.

Rackspace supports SDKs for the following languages:

-  Go

-  Java

-  .Net

-  Node.js

-  PHP

-  Python

-  Ruby

You can find links to all of the Rackspace-supported SDKs, with
installation instructions, guidance, tutorials and more for each, at
https://developer.rackspace.com/sdks/.

Direct API access
^^^^^^^^^^^^^^^^^
Each of our cloud services exposes an API which can be leveraged for
low-level integration with the service. The OpenStack API is a
“\ `REST <http://en.wikipedia.org/wiki/Representational_state_transfer>`__\ ”
(“Representational State Transfer”) API, meaning it is logically
structured, stateless, and scalable (among other properties).

For most use cases, we recommend leveraging one of our supported SDKs
versus integrating directly with the APIs. We have documented basic
functions for many APIs in many popular programming languages in
quickstart guides for developers at
https://developer.rackspace.com/docs/. However, knowing the API
structure, and being able to make direct, manual calls to the API is a
powerful tool for understanding and managing the Rackspace Cloud
infrastructure.

The API Developer Guide for each service is available at
http://docs.rackspace.com/; the same API operations are also listed
together at http://api.rackspace.com/.

While there are many ways to directly use the APIs, some of the most
common are:

-  command line tools like cURL

-  browser extensions like Postman for Chrome

-  utilities for your specific operating system are often available;
   check your app store or directory for “REST clients” and you’re sure
   to find one to your liking

The `API Developer Guides <http://docs.rackspace.com>`__ provide
examples and tutorials on accessing the APIs with cURL and other tools,
as well as sample calls and responses.

DevOps tools
^^^^^^^^^^^^
If you use popular DevOps tools such as Knife, Vagrant, Ansible, and
Salt, you may be interested in plugins (official or unofficial) for
these automation frameworks. Sources of more information about these
plugins include:

-  Knife: https://github.com/opscode/knife-rackspace

-  Vagrant: https://github.com/mitchellh/vagrant-rackspace

-  Ansible: http://docs.ansible.com/guide_rax.html

-  Salt: http://docs.saltstack.com/en/latest/topics/cloud/rackspace.html

Contents:

.. toctree::
   :maxdepth: 2

   setup_API
   cloudservers_API
   cloudnetworks_API
   cloudimages_API
   cloudblockstorage_API
   moreinfo_API
