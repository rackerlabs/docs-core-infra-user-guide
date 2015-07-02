.. cloud-images-sharing-planning:

--------------------------------------
Planning to share or use shared images
--------------------------------------
Although it is easy to share a cloud image, it is not always
appropriate. Consider carefully before creating an image-sharing
relationship.

Security and legal considerations for shared images
'''''''''''''''''''''''''''''''''''''''''''''''''''
Before sharing an image to another user, consider whether your image
includes any confidential or other content you should not share with
other users. For example, removing any stored passwords, source code, or
personal information are all good practices before creating and sharing
an image.

You should also consider whether there is any content in the image that
could be considered to violate confidentiality or other
legal agreements if it is shared to
another user.
Be especially careful not to share licensed software,
copyright-infringing content,
or untrusted software that may be malware.

If an image has been shared to you and you then consider sharing it to
your own consumer, consider the following before deciding to
export that image:

* The image should not contain software not intended to be distributed
  beyond the image producer and consumer.

* The image will be subject to any limitations on image export that
  already exist within Rackspace (for example, Windows Server images
  may not be able to be exported).

If you believe an image has been shared to you in error or with
malicious intent, contact Rackspace at
`cloudimageshelp@rackspace.com <mailto:cloudimageshelp%40rackspace.com>`__.

Financial considerations for shared images
''''''''''''''''''''''''''''''''''''''''''
Only the image producer is charged for the cost of the original shared
image (the cost to store the image in Cloud Files). Consumers of the
images do not incur a cost for either the sharing process, or using the
shared image until they:

* Create a cloud server from the shared image, at which point normal
  Cloud Servers pricing applies

* Take an image of a server created from the shared image, at
  which point the normal Cloud Files pricing to store the image applies

Regional considerations for shared images
'''''''''''''''''''''''''''''''''''''''''
Images can only be directly shared to consumers within
the same Rackspace cloud region as the producer.

If you need to use the same image in multiple regions,
you can create a copy of the image in each region.

:kc-article:`Transferring images between regions of the Rackspace open cloud <transferring-images-between-regions-of-the-rackspace-open-cloud>`
demonstrates a method of placing an image within a Cloud Files
container in one region and then retrieving it from the container 
in another region. This is a complex, multi-step method but it may be
worth the effort to master it if you need consistent images
in multiple regions.
