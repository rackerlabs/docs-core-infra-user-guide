.. _image_properties:

^^^^^^^^^^^^^^^^
Image properties
^^^^^^^^^^^^^^^^
When we talk about images in the Rackspace Cloud, what we’re really
referring to is an *image record* with which the image data file (for
example, a VHD) is associated. An image record consists of a set of
*image properties* (also known as *image metadata*) that describes the
image.

Image properties have several functions:

* They are used by the image owner to catalog the image. For example,
  public images provided by Rackspace have the
  ``com.rackspace\_\_1\_\_release\_id`` property which you can use to
  locate all available versions of a particular image. For images that
  you own, you may add your own cataloging properties so that you can
  efficiently search through your set of images.

* They are used by the Compute API to determine whether a request to
  boot a server from a particular image/flavor combination makes sense.
  For example, if the ``min\_ram`` property of an image is 512, then
  the specified flavor must provide at least 512 MB of RAM or the boot
  request will be rejected.

* They are used by the Compute Scheduler to locate a host for a server.
  For example, the ``hypervisor\_version\_requires`` property specifies
  what version of XenServer the image expects to find when it is
  booted.

* They are used by the hypervisor during the process of booting a
  server from an image. For example, the ``auto\_disk\_config``
  property indicates whether the hypervisor should expand the disk
  partition and filesystem found on the image to fit the server’s
  system disk.

* They are used by Cloud Images in its handling of images. For example,
  if the ``visibility`` property indicates that an image is public, the
  image will be included in each user’s image list.

A set of image properties is maintained by Cloud Images itself. Users
(and in some cases, even system administrators) cannot modify these
properties. Among these properties are:

* ``checksum``: the MD5 sum of the image data file

* ``status``: the current state of the image. An image must be in
  ``active`` status to be used to boot a server.

* ``owner``: indicates who owns the image

* ``id``: a universally unique identifier (UUID) assigned to this image
