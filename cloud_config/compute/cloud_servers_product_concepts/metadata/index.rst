Describing a Cloud Server with metadata
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
You can set and retrieve custom descriptive fields on your Cloud Server
instances by using metadata.

Metadata are key/value pairs that can be assigned to a Cloud Server
during creation, or at any point during the lifetime of the server. Both
the key field (sometimes called “name”) and the value field can be up to
255 characters in length.

This can be useful for adding descriptive tags to your Cloud Servers,
storing information about their configuration, and more.

Metadata stored on your Cloud Server is visible only to your account
members that would normally be able to see the Cloud Server details, and
to Rackspace Support. We suggest you follow normal information security
best practices and don’t store sensitive information such as passwords,
API keys, or confidential company information in metadata.

Metadata can also be created and stored on Cloud Images (such as
snapshots of your Cloud Server). For more information on working with
Cloud Images metadata (also known as “image properties”), see Image
properties.

Currently, the OpenStack command line nova utility or API must be used
to view, set, or delete metadata on a Cloud Server. For more information
on using the API to work with Cloud Server, metadata see
http://docs.rackspace.com/servers/api/v2/cs-devguide/content/MetadataSection.html.

Contents:

.. toctree::
   :maxdepth: 2

   show_metadata
   set_metadata
