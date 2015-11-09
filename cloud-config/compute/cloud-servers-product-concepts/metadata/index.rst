.. _cloud-servers-metadata:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Describing a Cloud Server with metadata
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You can set and retrieve custom descriptive fields on your Cloud Server
instances by using metadata.

Metadata are key/value pairs that can be assigned to a server
during creation, or at any point during the lifetime of the server. Both
the key field (sometimes called *name*) and the value field can be up to
255 characters in length.

Metadata can be useful for adding descriptive tags to your
servers,
storing information about their configuration, and more.

Metadata stored on your server is visible only to your account
members that would normally be able to see the Cloud Server details, and
to Rackspace Support. We suggest you follow normal information security
best practices and do not store sensitive information such as passwords,
API keys, or confidential company information in metadata.

Metadata can also be created and stored on Cloud Images (such as
snapshots of your Cloud Server). For more information on working with
Cloud Images metadata (also known image properties), see
:ref:`image_properties`.

Currently, the OpenStack command-line nova utility or API must be used
to view, set, or delete metadata on a cloud server. For more information
on using the API to work with server metadata, see the
:rax-dev-devguide:`metadata operations <cloud-servers/v2/developer-guide/#list-server-metadata>`
in the *Next Gen Cloud Servers API Developer Guide*.



.. toctree:: :hidden:
   :maxdepth: 2

   show-metadata
   set-metadata
