.. _cloud-images-sharing-planning:

++++++++++++++++++++++++++++++++++++++
Planning to share or use shared images
++++++++++++++++++++++++++++++++++++++
Although it is easy to share a cloud image, it is not always
appropriate. Consider the following points before creating an image-sharing
relationship.

Security and legal considerations for shared images
'''''''''''''''''''''''''''''''''''''''''''''''''''
Before sharing an image to another user, consider whether your image
includes any confidential or other content that you should not share with
other users. For example, you should remove any stored passwords,
source code, or personal information before creating and sharing
an image.

You should also consider whether the image contains any content that
could have legal implications if it is shared to another user, such as
licensed software, copyright-infringing content,
or untrusted software that may be malware.

If an image has been shared to you and you then consider sharing it to
your own consumer, consider the following before deciding to
export that image:

* The image should not contain software not intended to be distributed
  beyond the image producer and consumer.

* The image will be subject to any limitations on image export that
  already exist within Rackspace. For example, Windows Server images
  might not be able to be exported.

If you think that an image has been shared to you in error, or with
malicious intent, contact Rackspace at
`cloudimageshelp@rackspace.com <mailto:cloudimageshelp%40rackspace.com>`__.

Financial considerations for shared images
''''''''''''''''''''''''''''''''''''''''''
Only the image producer is charged for the cost of the original shared
image (the cost to store the image in Cloud Files). Consumers of the
images do not incur a cost for the sharing process, or for using the
shared image until they perform one of the following actions:

* Create a cloud server from the shared image, at which point normal
  Cloud Servers pricing applies

* Create an image of a server that was created from the shared image, at
  which point the normal Cloud Files pricing to store the image applies

Regional considerations for shared images
'''''''''''''''''''''''''''''''''''''''''
Images can only be directly shared to consumers within
the same Rackspace cloud region as the producer.

If you need to use the same image in multiple regions,
you can create a copy of the image in each region.

:how-to:`Transferring images between regions of the Rackspace open cloud <transferring-images-between-regions-of-the-rackspace-open-cloud>`
demonstrates a method of placing an image within a Cloud Files
container in one region and then retrieving it from the container
in another region. This is a complex, multi-step method but it might be
worth the effort to master it if you need consistent images
in multiple regions.

.. include:: /_common/seealso-concepts-cloud-images.txt
