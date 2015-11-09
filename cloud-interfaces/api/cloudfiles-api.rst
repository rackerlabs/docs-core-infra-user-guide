.. _cloudfiles-api:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Files and SDKs and APIs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you begin writing your own software to interact with Cloud Files,
you might want to learn about
how Cloud Files works in the Cloud Control Panel
and how SDKs and APIs are documented at Rackspace.

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

Just as you can use the Cloud Control Panel to help you
understand a manual process that you intend to automate, you can
use the API documentation to help you understand how
to use a software development kit (SDK) in your favorite
programming language.

* The API documentation describes *what* you can ask the API to do.
* The SDK documentation demonstrates *how* to ask the API to do
  something.

Awareness of both API and SDK capabilities can help
you plan the easiest way to develop your software.

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
In the :rax-api:`API cross-reference <>`, you can see all
available API operations for all cloud services. The operations
are grouped according to the service they interact with
(for example, Cloud Block Storage or Cloud File) and the scope
they act on, such as containers or objects.

You can see all Cloud Files operations in the
:rax-api:`API cross-reference <api-ref-files.html>`. In the group of
:rax-api:`operations that act on containers <api-ref-files.html#files_container_services>`,
you can see that:

* Sending a ``PUT`` request to the ``vi/{account}/{container}``
  requests the creation of a new container

* Sending a ``GET`` request to the same URI requests
  details for a specified container and lists the objects,
  sorted by name, within that container

.. figure:: /_images/cloudfileslistcontainersget.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations. Click
         detail to see more about how the API handles this request.

   *The API cross-reference lists all API operations. Click "detail"
   to see more about how the API handles each request.*

The request parameters and sample response shown here can
help you formulate a basic *List containers* request to the API and
understand the API's response.

In the sample response, ``bytes`` and ``name`` correspond
to the information available in the Cloud Control Panel.

In the :rax-docs:`Getting Started Guide for the Cloud Files API
<files/api/v1/cf-getting-started/content/Overview-d1e01.html>`,
you can see an example of
:rax-docs:`obtaining a list of account details and Cloud Files containers by using the cURL command-line interface (CLI)
<files/api/v1/cf-getting-started/content/Show-Account-Details-d1e101.html>`.

Learn about Cloud Files in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the
:rax-dev-quickstart:`SDK QuickStart for Cloud Files <cloud-files/getting-started>`,
you can see some of the same steps that are documented in
the API's Getting Started Guide. For example, both the API-focused and
SDK-focused documents show how to authenticate with your API
key before issuing any requests to the Cloud Files API.

The SDK QuickStart adds examples in several popular programming
languages, demonstrating how to use each language
to code some commonly-used requests to the Cloud Files API.

To see examples in a specific language, click that
language's name in the list across the top of the page.
For example, to see Cloud Files code samples in PHP, go to the
:rax-dev-quickstart:`SDK QuickStart for Cloud Files <cloud-files/getting-started>`
and click *PHP*.

.. figure:: /_images/cloudfilessdkphp.png
   :scale: 80%
   :alt: PHP is one of several languages for which we
         publish an SDK QuickStart.

   *PHP is one of several languages for which we
   publish an SDK QuickStart.*

Use SDK to help you write and run code to interact with Cloud Files
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests; for more
detailed guidance that will help you develop your software,
examine the SDK itself.

To find the full SDK for your programming language, start at
:rax-dev:`SDKs & Tools in the Developer Center <sdks>` and
find the language.

For example, if you code in PHP,

* Follow the installation instructions to give yourself a local
  copy of the php-opencloud SDK.
* In the `documentation repository for php-opencloud <http://docs.php-opencloud.com>`__,
  read about the *Volumes v1* service, applicable to both Rackspace and
  OpenStack configuration. In that document, you can go directly
  to an
  `example of listing Cloud Files <http://docs.php-opencloud.com/en/latest/services/object-store/containers.html#list-containers>`__.
