.. _cloud_images_sharing:

^^^^^^^^^^^^^^
Sharing images
^^^^^^^^^^^^^^
Cloud Images can be created as snapshots of a Cloud Server. They can
also be imported using the Cloud Images Import feature.

No matter how you create a Cloud Image, you can share it from one
Rackspace Cloud account to another, on an on-demand basis. This can be
useful for many scenarios:

* Share an image of a new server you have created or customized to a
  colleague for testing and comments.

* If you have multiple cloud accounts at Rackspace, for example to
  support different internal organizations or company branches, you can
  create a single central image and then share it with other accounts
  so they don’t have to create one themselves.

An image producer is also called an image owner. An image owner can
share an image with one or more image consumers.

An image consumer is also called an image member.

A shared image is an image that an image owner has made available to one
or more image members.

Exporting shared images
-----------------------
If a consumer has created a Cloud Server image/snapshot from a shared
image, they should consider the following concerns if they choose to
export that image:

* The image should not contain software not intended to be distributed
  beyond the image producer and consumer.

* The image will be subject to any limitations on image export that
  already exist within Rackspace (for example, Windows Server images
  may not be able to be exported).

Preparing to share an image
'''''''''''''''''''''''''''
Before you can share an image to one (or more) users, you will need to
complete some preparatory steps:

1. Create a snapshot of a Cloud Server, or import an image that you will
   be sharing.

2. Note the UUID (also known as “image ID”) of the image that you will
   be sharing. The UUID can be gathered from the API or Cloud Control
   Panel.

3. Gather the tenant ID(s) (also known as “DDI” or “customer number”) of
   the consumer(s) to whom you will be sharing. This is a numeric ID
   that the consumer can find in their Control Panel or using their API.
   Note: The target consumer must provide their tenant ID to you; you
   are not able to search, browse, or otherwise discover their unique
   ID.

Offering to share an image
''''''''''''''''''''''''''
Once the image producer has the proper information, the sharing process
is very straightforward.

1. The image producer uses the API or tools to issue the image share
   request to one or more image consumers.

2. The image consumer uses the API or tools to either accept or reject
   the image, determining whether it will be available in their image
   list (their “member status”).

The image producer repeats this process for each additional image, and
for each additional consumer that needs to be added as a member to each
image.

Removing members from a shared image
''''''''''''''''''''''''''''''''''''
An image can have some or all of its members removed using the API or
tools. The image producer has complete control over this action, and is
the only one that can delete members from the image.

Any members that *rejected* the share request are technically still
members, even though they will not have visibility or access to the
image. The image producer can and should delete these members from the
image if they no longer have reason to be included.

Getting support for shared images
'''''''''''''''''''''''''''''''''
Rackspace supports the images we offer as base images.

In almost all cases, an image that is shared from a producer to
consumers is one that has been modified from a base Rackspace image or
is a custom image that has been imported.

This means that providing detailed support for modifications or
applications in the shared image may be beyond the scope of Rackspace
support (in either Managed Infrastructure or Managed Operations).
Rackspace will generally offer best-effort support to verify whether any
Cloud Servers created from the images have problems booting or other
issues, but detailed troubleshooting of any specific additional
functionality may be the responsibility of the image producer.

Contents:

.. toctree::
   :maxdepth: 2

   models
   planning
