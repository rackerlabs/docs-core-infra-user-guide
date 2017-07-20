.. _cloudfiles-cli:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Files and CLIs: swift and swiftly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To interact with Cloud Files at the command line, you can
use tools created specifically for the purpose of interacting
with OpenStack-based clouds, such as Rackspace CLI (rack), swift, and
swiftly, or general-purpose tools (cURL).

For more information about these tools, see the following
resources:

* :ref:`rack`
* :ref:`swift`
* :ref:`swiftly`

Before you can use one of these tools, you must install a
local (client) copy. The installation procedure varies for each
tool and is documented with with the tool.

The commands you can send are the same as the requests you can send to the API
endpoint, but are wrapped in the syntax of the client.
The :rax-docs:`Cloud Files API Reference <cloud-files/v1/storage-api-reference/>`
lists those requests for Cloud Files.

The *Getting Started Guide for the Cloud Files API* includes many
examples of using cURL, especially at
:rax-docs:`Using the API directly by using cURL <files/api/v1/cf-getting-started/content/Using_the_API_Directly.html>`.



.. toctree:: :hidden:
   :maxdepth: 2

   swift
   swiftly
