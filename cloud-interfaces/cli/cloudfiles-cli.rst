.. _cloudfiles-cli:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Files and CLIs: swift and swiftly
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To interact with Cloud Files at the command line, you can use tools
created specifically for the purpose of interacting with OpenStack-based
clouds (nova, swift) or general-purpose tools (cURL).

Because Cloud Servers and Cloud Files work so closely together,
the command-line tools that work well with Cloud Servers also
work well with Cloud Files.

You can read about these as a group at :ref:`cloudservers-cli`
or you can go directly to the tool that interests you:

* :ref:`nova`
* :ref:`supernova`
* :ref:`curl`

You can also use the :ref:`swift` or :ref:`swiftly`, focused on Cloud Files.

In working with Cloud Files, you may find that you need to use
nova for some functions and swift for others. You should install
them both.

Before you can use one of these tools, you must install a
local (client) copy. The installation procedure varies for each
tool and is documented with with the tool.

The commands you can send are the same, wrapped in the syntax
of the client, as the requests you can send to the API
endpoint. The :rax-api:`API cross-reference <api-ref-files.html>`
lists those requests for Cloud Files.

The *Getting Started Guide for the Cloud Files API* includes many
examples of using cURL, especially at
:rax-docs:`Using the API directly by using cURL <files/api/v1/cf-getting-started/content/Using_the_API_Directly.html>`.








.. toctree:: :hidden:
   :maxdepth: 2

   swift
   swiftly
