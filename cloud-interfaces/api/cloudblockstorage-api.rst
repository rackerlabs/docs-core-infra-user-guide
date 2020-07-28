.. _cloudblockstorage-api:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Block Storage and APIs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you begin writing your own software
to interact with Cloud Block Storage,
you might want to learn about
how Cloud Block Storage works
in the Cloud Control Panel
and how APIs are documented at Rackspace.

.. _cloudblockstorage-api-investigation:

+++++++++++++++++++++++++++++++++++++
Cloud Block Storage API investigation
+++++++++++++++++++++++++++++++++++++
Using an API, you can write software to automate functions that could otherwise
be performed manually by a person logged in to the Cloud Control Panel.
You can accelerate your understanding of how the API works
by using the Cloud Control Panel to demonstrate the manual process
before you begin to automate it;
to interact with the Cloud Block Storage service,
the Cloud Control Panel sends requests via the same API
that you interact with when you write your own software.

Sometimes, especially for new features that are not yet available
in the Cloud Control Panel,
you can write software to perform functions
using the API
that could not be performed in any other way.
Product announcements for Limited Availability
and Early Access releases point out this limitation when it applies.
In that case,
experimenting in the Cloud Control Panel can show you
only part of the process of working with a new feature;
other details are described in the
:rax-docs:`API documentation <>`.

Just as you can use the Cloud Control Panel
to help you understand a manual process that you intend to automate,
you can use the API documentation to help you understand
how to use API operations to automate cloud functions.

The API documentation describes what you can accomplish, how to structure an 
API operation, and what responses to expect.

.. _cloudblockstorage-api-demonstration:

+++++++++++++++++++++++++++++++++++++
Cloud Block Storage API demonstration
+++++++++++++++++++++++++++++++++++++
Using the process suggested at
:ref:`cloudblockstorage-api-investigation`,
this section provides an example of how you can plan
and then write your own software to perform one simple task:
list all your Cloud Block Storage volumes.

Learn about Cloud Block Storage in the Cloud Control Panel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the
:mycloud:`Cloud Control Panel <>`,
your session begins with information about your Cloud Servers.
To see your Cloud Block Storage information, click **Storage**
and then click **Block Storage Volumes**.

.. figure:: /_images/storageblockstoragevolumes.png
   :scale: 80%
   :alt: To move from Cloud Servers to
         Cloud Block Storage details,
         click Storage and then click Block Storage Volumes.

   *To move from Cloud Servers to
   Cloud Block Storage details,
   click "Storage" and then click "Block Storage Volumes".*

By default, the list is focused on your account's home region,
showing all volumes in that region;
you can select a different region and you can search for a
specific volume.

.. figure:: /_images/cloudblockstorage0volumes.png
   :scale: 80%
   :alt: If you have no Cloud Block Storage volumes,
         the Cloud Control Panel shows you how to
         create one.

   *If you have no Cloud Block Storage volumes,
   the Cloud Control Panel shows you how to
   create one.*

If your list of volumes is not empty, then for each volume
you can see:

* Its ID
* The name of the server to which it is attached
* The region in which it is located
* The type of disk it uses
* Its size

.. figure:: /_images/cloudblockstorage1volume.png
   :scale: 80%
   :alt: The Cloud Control Panel lists all of your
         Cloud Block Storage volumes.

   *The Cloud Control Panel lists all of your
   Cloud Block Storage volumes.*

.. include:: /_common/note-chrome-devtools.txt

Learn about Cloud Block Storage in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the :rax-docs:`API documentation <>`,
you can see all available API operations for all cloud services.
The operations are grouped according to the service they interact
with (for example, Cloud Block Storage or Cloud Files)
and the scope they act on (for example, volumes or snapshots).

You can see all Cloud Block Storage operations in the
:rax-docs:`Cloud Block Storage API Reference <cloud-block-storage/v1/api-reference/>`.
In the group of
:rax-docs:`Volumes operations <cloud-block-storage/v1/api-reference/cbs-volumes-operations/>`,
you can see that:

* Sending a ``POST`` request to the ``v1/{tenant_id}/volumes``
  URI requests creation of a new server

* Sending a ``GET`` request to the same URI
  requests a basic list of information about volumes

* Sending a ``GET`` request to the same URI and appending ``/detail``
  requests an expanded list of information about volumes

On the first ``GET`` line, click **detail** to see
more about how the API handles this request.
The request parameters and sample response shown here can
help you formulate a basic *List volumes* request to the API
and understand the API's
response.

In the sample response,
``id``, ``display_name``, ``size``, and ``volume_type``
correspond to the information available on the Cloud Control Panel.

In the
:rax-docs:`Getting Started Guide for the Cloud Block Storage API <cloud-block-storage/v1/getting-started/>`,
you can see an example with the cURL command-line interface (CLI) for
:rax-docs:`Listing existing block storage volumes
<cloud-block-storage/v1/getting-started/use-API-directly/#listing-existing-block-storage-volumes>`.
