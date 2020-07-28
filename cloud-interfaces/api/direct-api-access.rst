.. _direct-api-access:

^^^^^^^^^^^^^^^^^
Direct API access
^^^^^^^^^^^^^^^^^
Each of our cloud services exposes an API that can be leveraged for
low-level integration with the service.
Rackspace APIs,
like OpenStack APIs,
are Representational State Transfer (REST) APIs,
meaning that they are logically
structured, stateless, and scalable (among other properties).

In the :rax-dev:`Developer Center <docs>`, you can learn about the API
structure and being able to make direct, manual calls to the API is a
powerful tool for understanding and managing the Rackspace cloud
infrastructure.

The API Developer Guide for each service is published in
:rax-docs:`our technical documentation collection <>`.

Some of the most common ways to directly interact with APIs are:

* Command line tools,
  such as
  `cURL <http://curl.haxx.se/>`__

* Browser extensions,
  such as
  `Postman for Chrome <https://www.getpostman.com/>`__

* Utilities for specific operating systems,
  such as those listed in your app store or directory
  under **REST client**

For each service that offers a public API,
Rackspace publishes at least two technical documents:

* :rax-docs:`API developer guide <>`:
  reference material *describing* API requests and sample responses

* :rax-docs:`API getting started guide <>`:
  tutorial material *demonstrating* simple interactions
  with the API

For most APIs, we also publish
:rax-docs:`API release notes <>`,
*announcing* changes to the API.

These API documents primarily support readers who are
already experienced with RESTful APIs in other contexts and
are seeking details specifically about the Rackspace APIs.
We don't provide a beginner-level API tutorial,
however, REST is widely used and introductory material is
readily available.
If you want to work with our APIs and this is your first
experience with RESTful APIs,
begin with :ref:`setup-api`.
