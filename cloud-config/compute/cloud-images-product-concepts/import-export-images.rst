.. _import-export-images:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Importing and exporting images
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The Rackspace cloud runs on OpenStack, open-source software that
runs in many data centers in addition to Rackspace data
centers. In addition to running on open-source software, our cloud is
open in the following ways:

* You can export a virtual machine image that you own out of the
  Rackspace cloud. You might want to do this, for example, if you’d
  like to store an image in a non-Rackspace location.

* You can import a properly prepared virtual machine image into the
  Rackspace cloud. You might want to do this if you want to move a
  workload into the Rackspace cloud from another cloud provider, or if
  you prefer to prepare your virtual machine images on your own
  hardware.

You can find more information about image importing and exporting in the
:how-to:`Cloud Images FAQ <cloud-images-faq>`.

Exporting an image
''''''''''''''''''
When you tell Rackspace Cloud Images to export one of your virtual
machine images, the service retrieves the image from its Cloud
Images storage location, prepares the image for export, and place sthe
image in your Rackspace Cloud Files account. You can download
it from Cloud Files to export it.

Not all images can be exported. Rackspace has licensing agreements
with some providers of Rackspace public images that prohibit us from
exporting any images of servers created from these public images. For
example, Windows Server images cannot be exported.

Additionally, you cannot export an image that you do not own. For
example, you cannot export a Rackspace public image or an image that has
been shared with you.

Importing an image
''''''''''''''''''
When you use Rackspace Cloud Images to import a virtual machine image,
Cloud Images stores your image data in a special location and creates an
image record so that your image can be used to boot servers in the
Rackspace cloud. Thus, to import an image, you must perform the
following actions:

* Upload your image data to your Cloud Files account

* Create a Cloud Images import task

An image must consist of a single file in the VHD format, and the image import
limit is 160 GB.

Export-import asymmetry
'''''''''''''''''''''''
Although you can export a virtual machine image that you own (subject to
licensing restrictions), you might not be able to import that image back
into the Rackspace public cloud. Cloud Server flavors that have system disks
exceeding 160 GB can be difficult to export. You might need to request a manual
export from the hypervisor, which has a maximum import size of 160 GB. License
restrictions prevent you from exporting Windows or RedHat Images.

.. include:: /_common/seealso-concepts-cloud-images.txt
