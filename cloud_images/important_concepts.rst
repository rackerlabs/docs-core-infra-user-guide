Important Concepts
==================

A virtual machine image ("image", for short) is a single file that contains
a virtual disk that has a bootable operating system on it.  Images come in
various formats.  In the Rackspace open cloud, we use images in the VHD
format.

VHD
---

VHD is the Virtual Hard Disk format.  It was developed by Microsoft and
is used by the Microsoft Hyper-V and Citrix XenServer hypervisors, among
others.

Image Properties
-------------------

When we talk about images in OpenStack, what we're really referring to is
an *image record* with which the image data file (for example, a VHD) is
associated.  An image record consists of a set of *image properties* (also
known as *image metadata*) that describes the image.

Image properties have several functions.

- They are used by the image owner to catalog the image.  For example,
  public images provided by Rackspace have the **com.rackspace__1__release_id**
  property which you can use to locate all available versions of a particular
  image.  For images that you own, you may add your own cataloging properties
  so that you can efficiently search through your set of images.
  
- They are used by the Compute API to determine whether a request to
  boot a server from a particular image/flavor combination makes
  sense.  For example, if the **min_ram** property of an image is 512,
  then the specified flavor must provide at least 512 MB of RAM or the
  boot request will be rejected.

- They are used by the Compute Scheduler to locate a host for a server.
  For example, the **hypervisor_version_requires** property specifies what
  version of XenServer the image expects to find when it's booted.

- They are used by the hypervisor during the process of booting a server
  from an image.  For example, the **auto_disk_config** property indicates
  whether the hypervisor should expand the disk partition and filesystem
  found on the image to fit the server's system disk.

- They are used by the OpenStack Image Cataloging and Delivery Service (also
  known as Glance) in its handling of images.  For example, if the
  **visibility** property indicates that an image is public, the image will
  be included in each user's image list.

There's a set of image properties that are maintained by Glance itself.  Users
(and in some cases, even system administrators) cannot modify these properties.
Among these properties are:

- **checksum**: the MD5 sum of the image data file

- **status**: the current state of the image.  An image must be in **active**
  status in order to be used to boot a server.

- **owner**: indicates who owns the image

- **id**: a universally unique identifier (UUID) assigned to this image

Immutability
------------

An important aspect of how Glance treats images is that *image data is
immutable*.  Hence, once the image data has been uploaded and the checksum
and location are set, the image data *may not be modified*.  Thus you are
guaranteed that whenever you boot a server from the image with id
da455637-9ff1-43e9-bb81-0f9e5498a913, you will always receive the exact
same set of bits (and hence, the exact same operating system kernal and
configuration) every single time.

This is an important thing to keep in mind if you plan to create your own
set of custom images.  If you create an image and then discover, for example,
that it's missing a security update so important that you don't want anyone
to use the original image, you can't simply swap out the image data.  Instead,
you must delete the original image and create a new one.  The new image, of
course, will be assigned a different UUID.  Thus, if you are writing scripts
to use an image containing the SuperOS operating system, it's a good
idea *not* to use the image UUID in your script.  Instead, you should use
some custom image property to identify an image as containing the SuperOS
operating system, and then program your script to use the filtering abilities
of the Images API to locate the image you want.

