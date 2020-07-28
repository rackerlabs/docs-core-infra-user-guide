.. _cloudfiles-api:

^^^^^^^^^^^^^^^^^^^^
Cloud Files and APIs
^^^^^^^^^^^^^^^^^^^^
When you begin writing your own software to interact with Cloud Files,
you might want to learn about
how Cloud Files works in the Cloud Control Panel
and how APIs are documented at Rackspace.

.. _cloudfiles-api-investigation:

+++++++++++++++++++++++++++++
Cloud Files API Investigation
+++++++++++++++++++++++++++++
Using an API, you can write software to automate function that
could otherwise be performed manually by a person logged in to
the Cloud Control Panel. You can accelerate your
understanding of how the API works by using the Cloud Control
Panel to demonstrate the manual process before you begin to automate
it; to interact with the Cloud Files service, the Cloud
Control Panel sense requests using the same API that you interact
with when you write your own software.

Sometimes, especially for new features that are not yet
available in the Cloud Control Panel, you can write software
to perform functions using the API that could not
be performed in any other way. Product announcements for
Limited Availablility and Early Access releases point out this
limitation when it applies. In that case, experimenting
in the Cloud Control panel can show you only part of the process
of working with a new feature; other details are described
in the :rax-docs:`API documentation <>`.

Just as you can use the Cloud Control Panel
to help you understand a manual process that you intend to automate,
you can use the API documentation to help you understand
how to use API operations to automate cloud functions.

The API documentation describes what you can accomplish, how to structure an 
API operation, and what responses to expect.

.. _cloudfiles-api-demonstration:

+++++++++++++++++++++++++++++
Cloud Files API demonstration
+++++++++++++++++++++++++++++
Using the process suggested at :ref:`cloudfiles-api-investigation`,
this section provides an example of how you can plan and then write
your own software to perform one simple task:
list all your Cloud Files containers.

Learn about Cloud Files in the Cloud Control Panel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the :mycloud:`Cloud Control Panel<>`, your
session begins with information about your Cloud Servers.

.. figure:: /_images/controlpanelcloudfiles.png
   :scale: 80%
   :alt: To see your Cloud Files information, click Storage
         and then click Files.

   *To see your Cloud Files information, click "Storage"
   and then click "Files".*


If your list of containers is not empty, then for each
container you can see:

* Its name
* The region in which it is located
* The number of files stored within
* Its size

.. include:: /_common/note-chrome-devtools.txt

Learn about Cloud Files in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the :rax-docs:`API documentation <>`, you can see all
available API operations for all cloud services. The operations
are grouped according to the service they interact with
(for example, Cloud Block Storage or Cloud File) and the scope
they act on, such as containers or objects.

You can see all Cloud Files operations in the
:rax-docs:`Cloud Files API Reference <cloud-files/v1/storage-api-reference/>`.
In the group of
:rax-docs:`Containers operations <cloud-files/v1/storage-api-reference/container-services-operations/>`,
you can see that:

* Sending a ``PUT`` request to the ``vi/{account}/{container}``
  requests the creation of a new container

* Sending a ``GET`` request to the same URI requests
  details for a specified container and lists the objects,
  sorted by name, within that container

The request parameters and sample response shown here can
help you formulate a basic *List containers* request to the API and
understand the API's response.

In the sample response, ``bytes`` and ``name`` correspond
to the information available in the Cloud Control Panel.

In the :rax-docs:`Getting Started Guide for the Cloud Files API
<cloud-files/v1/getting-started/use-API-directly/>`,
you can see an example with the cURL command-line interface (CLI) for
:rax-docs:`Creating a storage container
<cloud-files/v1/getting-started/use-API-directly/#creating-a-storage-container>`.
