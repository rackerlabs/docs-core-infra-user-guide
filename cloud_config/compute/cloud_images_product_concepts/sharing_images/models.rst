.. _cloud_images_sharing_models:

------------------------------
Models of sharing Cloud Images
------------------------------
When you share a Cloud Image, 
you create direct, unique relationship with each
consumer of the image.
The relationship between the producer of an image 
and each consumer of the image 
evolves through multiple stages.

“1 to 1” sharing
''''''''''''''''
When you share an image, what you are doing is creating a relationship
between you and one or more additional users that gives those users
rights to see and use the image. Those users become “members” of that
relationship.

This model is known as “1 to 1” sharing because, even though you can
share an image to multiple people, you are actually creating one
relationship for each user. For example, if Producer A shares an image
to Consumer A and Consumer B, the relationships that are created are:

* Producer A –> shared image –> Consumer A

* Producer A –> shared image –> Consumer B

This means that:

* You can revoke the rights to the shared image from one consumer
  without affecting its availability to other users.

* The image is available only to the specific consumer to whom you’ve
  shared it. It is not a “1 to many” sharing where you are able to
  share an image to ALL other Cloud users.

Handshaking
'''''''''''
Sharing an image was designed with a “handshake” process model, to
ensure that users involved in a sharing request have both awareness and
control throughout.

.. image:: ../../../../figures/CloudImagesHandshaking.png
   :alt: The image producer creates an image 
         and creates an image member for the image consumer; 
         the image consumer accepts or rejects the image.

1. The image producer identifies the desired image, and the consumers to
   whom the image will be shared.

2. The image producer issues one or more requests to add those consumers
   as “members” to the image.

3. Each of the consumers can choose to “accept” or “reject” the image
   sharing request. This is known as their “member status”. The member
   status controls whether image appears in the consumer’s image list.

Image members can have any of the following statuses:

* **accepted**: The consumer accepts the invitation to potentially use
  the offered image, and the image appears in the consumer’s image
  list. The producer knows that the consumer made an active decision
  about the image.

* **rejected**: The consumer declines the invitation to potentially use
  the offered image, and the image does not appears in the consumer’s
  image list. The producer knows that the consumer made an active
  decision about the image. Note: The consumer can still use the image,
  but must know the image ID, since the image is not in the image list.

* **pending**: The consumer neither accepts nor declines the invitation
  to potentially use the offered image, and may not have even noticed
  the offer. The producer might elect to send a reminder that the image
  is available, but this is outside the scope of the Cloud Images API.
   
.. NOTE:: 
   While an image is pending, the consumer can use the image, 
   but must know the image ID since the image is not shown in the image list.
