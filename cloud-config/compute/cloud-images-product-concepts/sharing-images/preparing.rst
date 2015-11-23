.. _cloud-images-sharing-preparing:

+++++++++++++++++++++++++
Preparing to share images
+++++++++++++++++++++++++
Before an image producer can share an image to one or more consumers,
the producer must
perform some preparatory steps:

1. Create the image to be shared.
   This can be done by saving a snapshot of a cloud server
   or by importing an image.

2. Obtain the UUID (also known as the image ID) of the image
   to be shared.
   The UUID is available from the API or
   the Cloud Control Panel.

3. Get the tenant ID (also known as the DDI or customer number) of
   the consumer or consumers to whom
   the image will be shared.
   This is a numeric ID
   that the consumer can find in their Cloud Control Panel
   or by using the API.

   .. NOTE::
      The target consumer must provide their tenant ID to
      the producer;
      the producer cannot search, browse, or otherwise discover
      a consumer's unique ID.

.. include:: /_common/seealso-concepts-cloud-images.txt
