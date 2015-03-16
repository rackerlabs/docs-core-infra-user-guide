Setting and updating metadata
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
To set or change metadata on a Cloud Server, use the *nova meta* command
with the action *set*, and provide the Cloud Server ID and key/value
pair you want to set or update:

xxxxxxxx insert screenshot here setting a sample field like
my\_server\_role=webserver or something similar.

In general, you can use any metadata key you need, as long as it doesn’t
conflict with existing metadata placed on the Cloud Server by Rackspace,
and doesn’t exceed 255 characters.

To delete a metadata key from a Cloud Server, use the *nova meta*
command with the action *delete*, and provide the Cloud Server ID and
the key you want to remove:

xxxxxxxx insert screenshot of deleting a metadata field, possibly the
one we used earlier as an example.

After a metadata field is deleted, it cannot be recovered, unless you
have a stored image of the server. If you have a stored image of the
server, you may be able to

* rebuild the server from the image and retrieve the metadata field

* view the image properties of the image and look for fields prefixed
   with instance
