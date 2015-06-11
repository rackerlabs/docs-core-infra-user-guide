.. _import_export_images:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Importing and exporting images
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The Rackspace Cloud proudly runs on OpenStack, open-source software that
can and does run in many data centers in addition to Rackspace data
centers. In addition to running on open-source software, our cloud is
open in the following ways:

* You can export a virtual machine image that you own out of the
  Rackspace Cloud. You might want to do this, for example, if you’d
  like to store an image in a non-Rackspace location.

* You can import a properly-prepared virtual machine image into the
  Rackspace Cloud. You might want to do this if you want to move a
  workload into the Rackspace Cloud from another cloud provider, or if
  you prefer to prepare your virtual machine images on your own
  hardware.

You can find more information concerning image import and export in the
`Cloud Images
FAQ <http://www.rackspace.com/knowledge_center/article/cloud-images-frequently-asked-questions>`__.

Exporting an image
''''''''''''''''''
When you tell Rackspace Cloud Images to export one of your virtual
machine images, the service will retrieve the image from its Cloud
Images storage location, prepare the image for export, and place the
image in your personal Rackspace Cloud Files account. You can download
it from Cloud Files for whatever purpose you wanted to export your
image.

Not all images can be exported. Rackspace may have licensing agreements
with some providers of Rackspace public images that prohibit us from
exporting any images of servers created from these public images. For
example, Windows server images cannot be exported.

Additionally, you cannot export an image that you do not own. So, for
example, you cannot export a Rackspace public image or an image that has
been shared with you.

Importing an image
''''''''''''''''''
When you use Rackspace Cloud Images to import a virtual machine image,
Cloud Images stores your image data in a special location and creates an
image record so that your image can be used to boot servers in the
Rackspace Cloud. Thus, to import an image, you must do the following:

* Upload your image data to your Cloud Files account

* Create a Cloud Images import task

There are some restrictions on image import. An image must consist of a
single file in the VHD format. Additionally, it cannot have an actual
(or virtual) size greater than 40 GB. 40GB is the maximum size of a
Performance flavor system disk.

Export-import asymmetry
'''''''''''''''''''''''
While you can export a virtual machine image that you own (subject to
licensing restrictions), you may not be able to import that image back
into the Rackspace public cloud. That’s because some of the standard
flavors have system disks that exceed 40 GB. 40GB is the maximum size of
a Performance flavor system disk.
