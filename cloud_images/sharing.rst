Sharing
=======

Cloud Images (i.e. snapshots/images created from a Cloud Server, or imported
using the Cloud Images Import feature) can be shared from
one Rackspace Cloud account to another, on an on-demand basis. This can be
useful for many scenarios:

* Share an image of a new server you have created or customized to a colleague
for testing and comments.

* If you have multiple Cloud accounts at Rackspace, for example to support 
different internal organizations or company branches, you can create a single
central image and then share it with other accounts so they don't have to create
one themselves. 

(Note, should we pillage more content from:
http://docs.rackspace.com/images/api/v2/ci-devguide/content/image-sharing.html
??)
also, this whole FAQ...
http://www.rackspace.com/knowledge_center/article/cloud-images-frequently-asked-questions#where-is-the-documentation

I'll try to include what I can here though)


Image sharing concepts
-------------------

Terminology
^^^^^^^^^^^

* **Image Producer**: A user that is sharing an image to one or more Image
Consumers.

* **Image Consumer**: A user to whom an image is being shared. Also known as an
image **"member"**

* **Shared image**: An image that an image owner has made available to one
or more image members


"1 to 1" sharing
^^^^^^^^^^^^^^^^

When you share an image, what you are doing is creating a relationship between
you and one or more additional users that gives those users rights to see and
use the image.  Those users become "members" of that relationship. 

This model is known as "1 to 1" sharing, because--even though you can share an
image to multiple people--you are actually creating one relationship for each
user. For example, if Producer A shares an image to Consumer A and Consumer B, the
relationships that are created are:

Producer A--->shared image--->Consumer A
Producer A--->shared image--->Consumer B

This means that:

* You can revoke the rights to the shared image from one consumer without affecting its
availability to other users.

* The image is available only to the specific consumer to whom you've shared it.
It is not a "1 to many" sharing where you are able to share an image to ALL
other Cloud users.

The sharing process
^^^^^^^^^^^^^^^^^^^

Sharing an image was designed with a "handshake" process model, to ensure that
users involved in a sharing request have both awareness and control throughout.  

illustration from/like:
http://docs.rackspace.com/images/api/v2/ci-devguide/content/figures/1/a/figures/image-member.png

1. The image producer identifies the desired image, and the consumers to whom the
image will be shared.  

2. The image producer issues one or more requests to add those consumers as "members"
to the image. 

3. Each of the consumers can choose to "accept" or "reject" the image sharing
request. This is known as their "member status". The member status controls
whether image appears in the consumer's image list. 

Image members can have any of the following statuses.

**accepted**: The consumer accepts the invitation to potentially use the offered image, and
the image appears in the consumer's image list. The producer knows that the
consumer made an active decision about the image.

**rejected**: The consumer declines the invitation to potentially use the offered image, and
the image does not appears in the consumer's image list. The producer knows
that the consumer made an active decision about the image.

[Note]	Note
The consumer can still use the image, but must know the image ID, since the
image is not in the image list.

**pending**: The consumer neither accepts nor declines the invitation to potentially use the
offered image, and may not have even noticed the offer. The producer might
elect to send a reminder that the image is available, but this is outside the
scope of the Cloud Images API.

[Note]	Note
The consumer can still use the image, but must know the image ID, since the
image is not in the image list.


Considerations before sharing or using shared images
--------------------------------------------------

Security & legal considerations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Before sharing an image to another user, you should always consider whether
your image has any confidential or other content to which you don't want other
users to have access. For example, removing any stored passwords, source code,
or personal information are all good practices before creating and sharing an
image. 

You should also consider whether there is any content in the image that could
be considered to have legal implications once it is shared to another user.
Examples can be licensed software, any unintended malware or suspicious
software, or any copyright infringing content. 

If you believe an image has been shared to you in error, or with malicious
intent, please contact Rackspace at cloudimageshelp@rackspace.com. 

Creating Cloud Servers from shared images
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Once an image is shared to a user, they are free to create Cloud Servers from
the shared image; they appear in the user's image list, just like any of their
own saved snapshots. After a Cloud Server is created from a shared image, any
subsequent snapshots that are taken of these new Cloud Servers will be
available only to that user, not the user that originally
shared the image.  

Any Cloud Servers or images created from the shared image will still be
available to the consumer, even if the shared image is revoked. 

Image sharing and Regions
^^^^^^^^^^^^^^^^^^^^^^^^^

Images can only be shared to consumers in the same Rackspace Cloud region. 

Costs incurred with shared images
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Only the image producer is charged for the cost of the original shared image
(usually the cost to store the image in Cloud Files). Consumers of the images
do not incur a cost for either the sharing process, or using the shared image
until they:

* create a Cloud Server from the shared image, at which point normal Cloud
Server pricing applies, or

* take an image of a Cloud Server created from the shared image, at which point
the normal Cloud Files pricing to store the image applies. 

Shared Images and Exporting
^^^^^^^^^^^^^^^^^^^^^^^^^^^

If a consumer has created a Cloud Server image/snapshot from a shared image,
they should consider the following concerns if they choose to export that
image:

* the image should not contain software not intended to be distributed beyond
the image producer and consumer

* the image will be subject to any limitations on image export that already
exist within Rackspace (for example, Windows Server images may not be able to
be exported)

Sharing an image
----------------

Sharing an image is accomplished using the Cloud Images API or OpenStack
command line tools. Support for Image Sharing in the Cloud Control Panel
will be released in the future. 

Preparing to share an image
^^^^^^^^^^^^^^^^^^^^^^^^^^^

In order to share an image to one (or more) users, you will need to complete
some preparatory steps:

1. Create a snapshot of a Cloud Server, or Import an image, that you will be
sharing. 

2. Note the UUID (also known as "image ID") of the image that you will be
sharing. The UUID can be gathered from the API or Cloud Control Panel. 

3. Gather the Tenant ID(s) (also known as "DDI" or "Customer number") of the
consumer(s) to whome you will be sharing. This is a numeric ID that can be found in
the consumer's Control Panel or using their API to determine their credentials.
*Note:* The target consumer must provide their Tenant ID to you; you are not able
to search, browse or otherwise discover their unique ID.
 
Sharing the image
^^^^^^^^^^^^^^^^^

Once the image producer has the proper information, the sharing process is very
straightforward.

1. The image producer uses the API or tools to issue the image share
request to one or more image consumers. 

2. The image consumers either accept or reject the image using the API or
tools, determining whether it will be available in their image list (their
"member status").

The image producer repeats this process for each additional image, or each
additional consumer that needs to be added as a member to each image. 

Removing members from  a shared image
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

An image can have some or all of its members removed using the API or tools.
The image producer has complete control over this action, and is the only one
that can delete members from the image. 

Any members that *rejected* the share request are technically still members,
even though they will not have visibility or access to the image. The image
producer can and should delete these members from the image if they no longer
have reason to be included.) 


Getting support for shared images
---------------------------------

In almost all cases, an image that is shared from a producer to a consumers is,
by definition, one that has been either modified from a base Rackspace image,
or a custom image that has been imported. 

This means that providing detailed support for any of the changes,
modifications, included functionality or applications in the shared image may
be beyond the scope of Rackspace support (in either Managed Infrastructure or
Managed Operations). Rackspace will generally offer best effort support to
verify if any Cloud Servers created from the images have problems booting or
other issues, but detailed troubleshooting of any specific additional
functionality may be the responsiblity of the customer. 
 


