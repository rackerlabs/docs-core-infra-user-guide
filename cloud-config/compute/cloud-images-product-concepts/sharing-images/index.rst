.. _cloud-images-sharing:

^^^^^^^^^^^^^^
Sharing images
^^^^^^^^^^^^^^
Cloud images can be created as snapshots of a cloud server. They can
also be imported using the Cloud Images Import feature.

No matter how you create an image, you can share it from one
Rackspace cloud account to another, on an on-demand basis. This can be
useful for many scenarios:

* Share an image of a new server you have created or customized to a
  colleague for testing and comments.

* If you have multiple cloud accounts at Rackspace, for example to
  support different internal organizations or company branches, you can
  create a single central image and then share it with other accounts
  so they do not have to create one themselves.

An image producer is also called an image owner. An image owner can
share an image with one or more image consumers.

An image consumer is also called an image member.

A shared image is an image that an image owner has made available to one
or more image members.

Preparing to share an image
'''''''''''''''''''''''''''
Before you can share an image to one (or more) users, you will need to
complete some preparatory steps:

1. Create a snapshot of a cloud server, or import an image that you will
   be sharing.

2. Obtain the UUID (also known as *image ID*) of the image that you will
   be sharing. The UUID is available from the API or 
   the Cloud Control Panel.

3. Gather the tenant ID(s) (also known as *DDI* or *customer number*) of
   the consumer(s) to whom you will be sharing. This is a numeric ID
   that the consumer can find in their Cloud Control Panel or using their API.
   
   .. NOTE::
      The target consumer must provide their tenant ID to you; 
      you cannot search, browse, or otherwise discover 
      their unique ID.


.. toctree:: :hidden:
   :maxdepth: 2

   models
   planning
   managing
   support
