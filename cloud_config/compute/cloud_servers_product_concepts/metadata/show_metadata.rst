.. _show_metadata:

^^^^^^^^^^^^^^^^
Showing metadata
^^^^^^^^^^^^^^^^
To view the metadata on a Cloud Server, use the *nova show* command with
the desired Cloud Server ID:

xxxxxx insert screenshot here of using commmand and output and highlight
the metadata fields

Some metadata are set by Rackspace and not available to be changed by
the user; generally these fields are used by automation and
orchestration systems needed to properly build and maintainer your Cloud
Server.

The metadata that are attached to your server are also stored if you
create a snapshot/image from the server, and restored when a server is
built from that image. The key names are prefixed with *instance\_*:

xxxxxxx show an example of the image metadata being viewed and the
instance
