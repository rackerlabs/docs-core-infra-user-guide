.. _cloud-files-product-actions:

~~~~~~~~~~~~~~~~~~~~~~~
Actions for Cloud Files
~~~~~~~~~~~~~~~~~~~~~~~
You can use Cloud Files to perform the actions below.

To learn how to perform Cloud Files actions using your choice of
interface, begin at

* :ref:`cloudfiles-gui`
* :ref:`cloudfiles-cli`
* :ref:`cloudfiles-api`

----

Create a Container
''''''''''''''''''
Before uploading any data to Cloud Files, you must create a storage
container. Containers cannot be created within another container, however
you can create up to 500,000 containers in your Cloud Files
account. Each container can store an unlimited number of objects.

Delete a Container
''''''''''''''''''
All objects within a container must be deleted before the container
itself can be deleted. Multiple containers allow for better
threading of the deletion scrips.

Deleting a container is a permanent action and cannot be reversed.

Create or Update an Object
''''''''''''''''''''''''''
Each container can store an unlimited number of objects.

For large files support, Cloud Files allows you to upload multiple file
segments and a manifest file to map the segments together. When
uploading large files:

* Files larger than 5 GB must first be segmented into smaller files
* File segments should not be smaller than 100-200 MB
* Files larger than 10 GB cannot be served from the CDN

Copy an Object
''''''''''''''

Delete an Object
''''''''''''''''
