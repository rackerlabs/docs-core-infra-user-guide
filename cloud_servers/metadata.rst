Metadata
========

Users have the ability to set and retrieve custom descriptive fields on their
Cloud Server instances by using "metadata". 

Metadata are key/value pairs that can be assigned to a Cloud Server during
creation, or at any point during the lifetime of the server. Both the key field
(sometimes called "name") and the value field can be up to 255 characters in
length. 

This can be useful for adding descriptive tags to your Cloud Servers, storing
information about their configuration, and more. 


Metadata stored on your Cloud Server is visible only to your account members
that would normally be able to see the Cloud Server details, and to Rackspace
Support. We suggest you follow normal information security best practices and
don't store sensitive information such as passwords, API keys, or confidential
company information in metadata. 

Note: Metadata can also be created and stored on Cloud Images (such as
snapshots of your Cloud Server). For more information on working with Cloud
Images metdata (also known as "image properties"), see [link to that section
when ready]. 

*Currently, the OpenStack command line nova utility or API must be used to
view, set, or delete metadata on a Cloud Server. For more information on using
the API to work with Cloud Server metadata see
http://docs.rackspace.com/servers/api/v2/cs-devguide/content/MetadataSection.html *

------------------------
Viewing metadata on a Cloud Server
----------------------------------

To view the metadata on a Cloud Server, use the *nova show* command with the desired
Cloud Server ID::

	insert screenshot here of using commmand and output and highlight the
	metadata fields

Some metadata will be set by Rackspace and not available to by changed by the
user; generally these fields are used by automation and orchestration systems
needed to properly build and maintainer your Cloud Server. 

The metadata that is attached to your server will be also be stored if you
create a snapshot/image from the server, and restored when a server is built
from that image. The key names will
be prefixed with *instance_*::   

	show an example of the image metadata being viewed and the instance_

----------------------------------
Setting and updating metadata on a Cloud Server
----------------------------------

To set or change metadata on a Cloud Server, use the *nova meta* command with
the action *set*, and provide the Cloud Server ID and key/value pair you want
to set or update::

	insert screenshot here setting a sample field like
	my_server_role=webserver or something similar. 

In general you are able to use any metadata key you need, as long as it doesn't
conflict with existing metadata placed on the Cloud Server by Rackspace, and
doesn't exceed 255 characters. 

--------------------------------
Deleting metadata on a Cloud Server
-----------------------------------

To delete a metadata key from a Cloud Server, use the *nova meta* command with
the action *delete*, and provide the Cloud Server ID and the key you want to
remove::

	insert screenshot of deleting a metadata field, possibly the one we
	used earlier as an example.

Once a metadata field is deleted, it can not be recovered, unless you have a
stored image of the server; in this case you may be able to 

* rebuild the server from the image and retrieve the metadata field
* or view the image properties of the image and look for fields prefixed with
   instance_


