.. _cloud-images-sharing-managing:

++++++++++++++++++++++
Managing shared images
++++++++++++++++++++++
After an image is shared to a consumer,
the consumer is free to create servers
from the shared image. The shared images are in the consumer's image list,
just as any of their own saved snapshots.

After a new server is created from a
shared image, any subsequent snapshots that are taken of that new cloud
server are available only to the
the shared image consumer, who is the
user that created them.
Snapshots of a server created from a shared image are not
available to the shared image producer, who is the user that
originally shared the image.

If the consumer creates any servers or images from the shared image
they remain
available to the consumer,
even if the producer revokes the shared image.

Offering to share an image
''''''''''''''''''''''''''
After the image producer has the correct information, the sharing process
is straightforward.

1. The image producer issues the image share
   request to one or more image consumers.

2. The image consumer either accepts or rejects
   the image, determining whether it will be available in their image
   list.
   The image consumer's acceptance or rejection of the offer to share
   the image is recorded in the image's
   member status.

The image producer repeats this process for each additional image and
for each additional consumer to be added as a member to each
image.

Removing members from a shared image
''''''''''''''''''''''''''''''''''''
An image can have some or all of its members removed using the API or
Cloud Control Panel. The image producer has complete control over
this action, and is
the only one who can delete members from the image.

Any members who *rejected* the share request are considered
members, even though they cannot see or access the
image. The image producer should delete these members from the
image if they no longer have reason to be included.

.. include:: /_common/seealso-concepts-cloud-images.txt
