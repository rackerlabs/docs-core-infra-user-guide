.. _cloudimages-cli:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Images and CLIs: glance
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To interact with Cloud Images at the command line,
you can use tools created specifically for the purpose
of interacting with OpenStack based clouds
(nova and glance)
or general-purpose tools (cURL).

.. note::

    Rackspace CLI does not currently support Cloud Images. Support for Cloud Images
    will be added as development for Rackspace CLI continues.

Because Cloud Servers and Cloud Images work so
closely together,
the command-line tools that work well with Cloud Servers
also work well with Cloud Images.

You can read about these as a group at
:ref:`cloudservers-cli`
or you can go directly to the tool that interests you:

* :ref:`nova`
* :ref:`supernova`
* :ref:`curl`

If you choose to use tools created specifically for interacting with Openstack
based clouds, use :ref:`glance`, focused on Cloud Images.

In working with Cloud Images,
you might find that you need to use nova for some functions
and glance for others. You should install them both.
You can see an example of using nova and glance together at
:rax-dev-blog:`OpenStack CLI Basics <openstack-cli-basics>`
where, in the "Creating a Modified Image" section,
``glance image-create`` establishes a new image
and ``nova boot`` initializes a new server from that image.

Before you can use one of these tools,
you must install a local (client) copy.
The installation procedure varies for each tool
and is documented with the tool.

The commands that you can send are the
the same as the requests you can send
to the API endpoint, but they are wrapped in the syntax of the client.
The :rax-docs:`Cloud Images API Reference <cloud-images/v2/api-reference/>`
lists those requests for Cloud Images.

The *Getting Started Guide for the Cloud Images API*
includes many examples of using cURL commands
to send requests to the API's endpoint,
especially at
:rax-docs:`Using images <images/api/v2/ci-gettingstarted/content/using-images.html>`.

The *Developers Guide for the Cloud Images API*
also demonstrates using cURL to interact with the API, such as at
:rax-dev-devguide:`How cURL commands work <cloud-images/v2/developer-guide/#document-general-api-info/how-curl-commands-work>`.



.. toctree:: :hidden:
   :maxdepth: 2

   glance
