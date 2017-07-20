.. _cloudservers-cli:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Servers and CLIs: rack, nova, and supernova
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To interact with Cloud Servers at the command line,
you can use Rackspace CLI (rack), tools created specifically for the purpose
of interacting with OpenStack based clouds
(nova and supernova)
or general-purpose tools (cURL).

Before you can use one of these tools,
you must install a local (client) copy.
The installation procedure varies for each tool
and is documented with the tool.

The commands that you can send are the
the same as the requests you can send
to the API endpoint, but they are wrapped in the syntax of the client.
The :rax-docs:`Cloud Servers API Reference <cloud-servers/v2/api-reference/>`
lists those requests for Cloud Servers.



.. toctree:: :hidden:
   :maxdepth: 2

   rack
   nova
   supernova
   curl
