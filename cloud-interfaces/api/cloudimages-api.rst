.. _cloudimages-api:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Images and SDKs and APIs
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you begin writing your own software
to interact with Cloud Images,
you might want to learn about
how Cloud Images works
in the Cloud Control Panel
and how SDKs and APIs are documented at Rackspace.

.. _cloudimages-api-investigation:

++++++++++++++++++++++++++++++
Cloud Images API investigation
++++++++++++++++++++++++++++++
Using an API,
you can write software to automate functions that could otherwise
be performed manually by a person logged in to the Cloud Control Panel.
You can accelerate your understanding of how the API works
by using the Cloud Control Panel to demonstrate the manual process
before you begin to automate it;
to interact with the Cloud Images service,
the Cloud Control Panel sends requests via the same API
that you interact with when you write your own software.

Sometimes,
especially for new features that are not yet available
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
in the :rax-docs:`API documentation <>`.

Just as you can use the Cloud Control Panel
to help you understand a manual process that you intend to automate,
you can use the API documentation to help you understand
how to use a software development kit (SDK)
in your favorite programming language.

* The API documentation describes
  *what* you can ask the API to do.

* The SDK documentation demonstrates
  *how* to ask the API to do something.

Awareness of both API and SDK capabilities
can help you to plan the easiest way to develop your software.

.. _cloudimages-api-demonstration:

++++++++++++++++++++++++++++++
Cloud Images API demonstration
++++++++++++++++++++++++++++++
Using the process suggested at
:ref:`cloudimages-api-investigation`,
this section provides an example of how you can plan
and then write your own software to perform one simple task:
list all your cloud images.

Learn about Cloud Images in the Cloud Control Panel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you login to the
:mycloud:`Cloud Control Panel <>`,
your session begins with information about your servers.
To see your Cloud Images information, click **Servers**
and then click **Saved Images**.

.. figure:: /_images/serverssavedimages.png
   :scale: 80%
   :alt: To move from Cloud Servers to
         Cloud Images details,
         click Servers and then click Saved Images.

   *To move from Cloud Servers to
   Cloud Images details,
   click "Servers" and then click "Saved Images".*

By default, the list is focused on your account's home region,
showing all images in that region;
you can select a different region and you can search for a
specific image.

If your list of images is not empty, then for each image
you can see:

* Its name
* The server from which it was created
* Its creation date
* Its size

.. figure:: /_images/cloudimageslistall.png
   :alt: The Cloud Control Panel lists all of your
         Cloud Networks networks.

   *The Cloud Control Panel lists all of your
   Cloud Networks networks.*

.. include:: /_common/note-chrome-devtools.txt

Learn about Cloud Images in API documentation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the :rax-docs:`API documentation <>`,
you can see all available API operations for all cloud services.
The operations are grouped according to the service they interact
with (for example, Cloud Images or Cloud Files)
and the scope they act on (for example, images or image schemas).

You can see all Cloud Images operations in the
:rax-docs:`Cloud Images API Reference <cloud-images/v2/api-reference/>`.
In the group of
:rax-docs:`Images operations <cloud-images/v2/api-reference/images-operations/>`,
you can see that:

* Sending a ``GET`` request to the ``images``
  URI requests a basic list of information about public images

* Sending a ``GET`` request to the same URI and appending an image ID
  requests an expanded list of information about a single image

.. figure:: /_images/cloudimageslistimagesget.png
   :scale: 80%
   :alt: api.rackspace.com lists all API operations.

   *The API cross-reference lists all API operations. Click "detail" to
   see more about how the API handles this request.*

The request parameters and sample response shown here can
help you formulate a basic *List images* request to the API
and understand the API's response.

In the sample response,
``name``, ``created_at``, ``size``, and ``id``
correspond to the information available on the Cloud Control Panel.

In the
:rax-docs:`Getting Started Guide for the Cloud Images <cloud-images/v2/getting-started/>`,
you can see an example with the cURL command-line interface (CLI) for
:rax-docs:`Listing images
<cloud-images/v2/getting-started/use-images/#listing-images>`.

Learn about Cloud Images in SDK QuickStart
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
In the
:rax-dev-quickstart:`SDK QuickStart for Cloud Images <cloud-images/getting-started>`,
you can see some of the same steps that are documented in
the API's Getting Started Guide.
For example, both the API-focused and SDK-focused documents
show how to authenticate with your API key before issuing any requests
to the Cloud Images API.

The SDK QuickStart adds examples in several popular programming
languages,
demonstrating how to use each language to
code some commonly-used requests to the
Cloud Images API.

To see examples in a specific language,
click that language's name in the list across the top of the page.
For example, to see Cloud Images code samples coded in python,
go to the
:rax-dev-quickstart:`SDK QuickStart for Cloud Images <cloud-images/getting-started>`
and click **PYTHON**.

.. figure:: /_images/cloudimagessdkpython.png
   :scale: 80%
   :alt: Python is one of several languages for which we
         publish an SDK QuickStart.

   *Python is one of several languages for which we
   publish an SDK QuickStart.*

Use SDK to help you write and run code to interact with Cloud Images
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The SDK QuickStart demonstrates a few basic requests;
for more detailed guidance that will help you
develop your software examine the SDK itself.

To find the full SDK for your programming language, start at
:rax-dev:`SDKs & Tools in the Developer Center <sdks>`
and find the language.

For example, if you code in python,

* Follow the installation instructions to give yourself
  a local copy of the pyrax (python for Rackspace) SDK.
* Click **documentation** to open the
  `GitHub repository for the pyrax SDK <https://github.com/rackspace/pyrax/>`__.
* In that pyrax repository, at
  `/docs/ <https://github.com/rackspace/pyrax/tree/master/docs>`__,
  you can see documents specific to
  three of the four core infrastructure services:
  Cloud Servers, Cloud Networks, Cloud Block Storage.
  Although no document is specific to Cloud Images,
  you can adapt the examples in one of the others.
