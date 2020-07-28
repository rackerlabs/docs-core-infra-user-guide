.. _cloudblockstorage-cli:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Block Storage and CLIs: cinder
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To interact with Cloud Block Storage at the command line,
you can use Rackspace CLI (rack), tools created specifically for the purpose
of interacting with OpenStack based clouds
(nova and cinder)
or general-purpose tools (cURL).

Because Cloud Servers and Cloud Block Storage work so
closely together,
the command-line tools that work well with Cloud Servers
also work well with Cloud Block Storage.

You can read about these as a group at
:ref:`cloudservers-cli`
or you can go directly to the tool that interests you:

* :ref:`rack`
* :ref:`nova`
* :ref:`supernova`
* :ref:`curl`

You can also use the :ref:`cinder`, focused on Cloud Block Storage.

Before you can use one of these tools,
you must install a local (client) copy.
The installation procedure varies for each tool
and is documented with the tool.

The commands that you can send are the
the same as the requests you can send
to the API endpoint, but they are wrapped in the syntax of the client.
The
:rax-docs:`Cloud Block Storage API Reference <cloud-block-storage/v1/api-reference/>`
lists those requests for Cloud Block Storage.

The *Getting Started Guide for the Cloud Block Storage API*
includes many examples of using cURL, especially at
:rax-docs:`Using the API directly by using cURL <cbs/api/v1.0/cbs-getting-started/content/Using_the_API_directly_d1e060.html>`.

If you have both the cinder client and a cURL client
installed on your local computer,
you can choose to issue commands either through your
local copy of the cinder client or by using a general-purpose client
such as cURL, by sending a request to the instance of
the python-cinderclient that is active at the API endpoint for
Cloud Block Storage.
You can see both methods demonstrated in the Cloud Block Storage
API documentation, under
:rax-dev-devguide:`Cloud Block Storage quotas <cloud-block-storage/v1/developer-guide/#document-general-api-info/cloud-block-storage-quotas>`.

* cinder users send a short command,
  reusing details provided when the cinder client was configured::

    cinder quota-usage yourAccountID

* cURL users send a long command or series of commands,
  specifying details required to perform the API request::

    curl -i -X GET https://dfw.blockstorage.api.rackspacecloud.com/v1/yourAccountID/os-quota-sets/yourAccountID?usage=True \
    -H "X-Auth-Project-Id: yourAccountID" \
    -H "User-Agent: python-cinderclient" \
    -H "Accept: application/json" \
    -H "X-Auth-Token: yourAuthToken"



.. toctree:: :hidden:
   :maxdepth: 2

   cinder
