.. _cloud-images-product-actions:

^^^^^^^^^^^^^^^^^^^^^^^^
Actions for Cloud Images
^^^^^^^^^^^^^^^^^^^^^^^^
You can perform the following actions to create and manage cloud images.
Actions can relate to an image, image sharing, image tags,
image tasks, and image schemas.

.. include:: /_common/note-rbac-actions.txt

To learn how to perform Cloud Images actions by using your choice of interface,
begin at one of the following topics:

* :ref:`cloudimages-gui`
* :ref:`cloudimages-cli`
* :ref:`cloudimages-api`

Create an image backup
----------------------
The create image action allows you to create an image of a cloud server (also
known as cloning a server). When you create an image from a server, you are
essentially saving that servers operating system for a later use. Creating an
image can also assist in restoring a server from a saved image.

* To find out how to create an image using the Cloud Control Panel click
  `here <http://www.rackspace.com/knowledge_center/article/create-an-image-of-a-server-and-restore-a-server-from-a-saved-image>`__.

* To find out how to create an image by using the API click
  `here <https://developer.rackspace.com/docs/cloud-servers/v2/api-reference/svr-basic-operations/#create-image-of-specified-server>`__.


Update an image
---------------
This action allows you to update an image that you own. Properties that can be updated
includes the name of the image, any associated tags included in the image,
the version of the operating system utilized by the sever, and minimum
disk and ram requirements which affects which flavors can be used with the image.

* The Cloud Control Panel can update certain properties of a saved image.  To do so,
  click on **Saved Images** under the Servers tab on the top of the page. On your list
  of saved images, click the cog next to the name of the image you wish to update. A
  drop down menu of attributes you can update will appear. Simply click the property
  you wish to update.

* To find out how to update an image by using the API click
  `here <https://developer.rackspace.com/docs/cloud-images/v2/api-reference/images-operations/#update-image>`__.

Create an image member
----------------------
This action allows you to add users to the list of members with whom the image
is shared. This process is also called *image sharing*. You can find more information on image sharing on the page,
:ref: `cloud-images-sharing-models`.

* To find out how to create an image member by using the Cloud Control panel click
  `here <https://support.rackspace.com/how-to/sharing-images-in-the-cloud-control-panel/>`__.

* To find out how to create an image member by using the API
  click `here <https://developer.rackspace.com/docs/cloud-images/v2/api-reference/image-sharing-operations/#create-image-member>`__.
