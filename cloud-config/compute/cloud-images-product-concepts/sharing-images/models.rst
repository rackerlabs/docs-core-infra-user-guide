.. _cloud-images-sharing-models:

++++++++++++++++++++++++
Models of sharing images
++++++++++++++++++++++++
When you share an image,
you are create a direct, unique relationship with each
consumer of the image.
The relationship between the producer of an image
and each consumer of the image
evolves through multiple stages.

1-to-1 sharing
''''''''''''''''''
When you share an image, you are creating a relationship
between you and one or more additional users that gives those users
rights to see and use the image. Those users become members of that
relationship.

This model is known as *1-to-1 sharing* because, even though you can
share an image to multiple people, you are actually creating one
relationship with each user. For example, if Producer A shares an image
to Consumer A and Consumer B, the following relationships are created:

* Producer A > shared image > Consumer A

* Producer A > shared image > Consumer B

.. figure:: /_images/cloudimagesharing.png
   :alt: The producer Jan has an independent
	 relationship with each consumer.

   *The producer Jan has an independent
   relationship with each consumer.*

Because every sharing relationship is independent:

* You can revoke the rights to the shared image from one consumer
  without affecting its availability to other users.

* The image is available only to the specific consumer to whom you
  have shared it. It is not 1-to-many sharing, where you are able to
  share an image to *all* other cloud users.

Handshaking
'''''''''''
Sharing an image was designed with a *handshake* process model, which
ensures that users involved in a sharing request have both awareness and
control throughout the process.

.. figure:: /_images/cloudimagehandshaking.png
   :alt: The image producer creates an image
         and creates an image member for the image consumer;
         the image consumer accepts or rejects the image.

   *The image producer creates an image
   and creates an image member for the image consumer.
   The image consumer accepts or rejects the image.*

1. The image producer identifies the image and the consumers to
   whom the image will be shared.

2. The image producer issues one or more requests to add those consumers
   as *members* of the image.

3. Each of the consumers can choose to *accept* or *reject* the image
   sharing request, which determines the consumer's member status.
   The member status controls whether the image
   appears in the consumer's image list.

Image members can have any of the following statuses:

* **Accepted**: The consumer accepts the invitation to potentially use
  the offered image, and the image appears in the consumer's image
  list. The producer knows that the consumer made an active decision
  about the image.

* **Rejected**: The consumer declines the invitation to potentially use
  the offered image, and the image does not appears in the consumer's
  image list. The producer knows that the consumer made an active
  decision about the image.

.. NOTE::
   While an image is in *rejected* status,
   the consumer can use the image
   but must know the image ID since the image is not in the image list.

* **Pending**: The consumer neither accepts nor declines the invitation
  to potentially use the offered image, and might not have noticed
  the offer. The producer might elect to send a reminder that the image
  is available, but this is outside the scope of the Cloud Images API.

.. NOTE::
   While an image is in *pending* status,
   the consumer can use the image
   but must know the image ID
   since the image is not shown in the image list.

.. include:: /_common/seealso-concepts-cloud-images.txt
