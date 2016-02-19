.. _web-acceleration:

~~~~~~~~~~~~~~~~
Web acceleration
~~~~~~~~~~~~~~~~
When using Cloud Files for web acceleration, you can use a basic organizational
structure to separate your content into different containers based on
object type, such as images, css, javascript, videos, or uploaded
content.

Building this structure enables you to quickly locate
your objects when you need them.

Container management
~~~~~~~~~~~~~~~~~~~~
A container is a storage compartment for your data and provides a
way for you to organize that data. You can think of a container as a
folder in Windows or a directory in Unix. The primary difference between
a container and these other file system concepts is that containers
cannot be nested.

You can create up to 500,000 containers under your account.

Using multiple containers
'''''''''''''''''''''''''
If you have an extremely large number of objects, it is most
effective to store them in multiple containers. When writing large
numbers of objects to a single container, the limit of 100 object
write requests per second per container may reduce overall performance.

Labeling containers
'''''''''''''''''''
When organizing your containers for an object storage solution,
give each container a two-part name:

- Identify the container's contents,
  such as the segment
  of the application accessing it.
- Attach an incremental number to plan ahead for multiple containers.

For example, if you begin with one container of data related to a
personnel-management application,
you might someday need multiple containers of data related to that application;
labeling the first personnel-related container `personnel-00000`
makes your labeling standard extensible as your data collection grows.

Keeping a local database of container structure
'''''''''''''''''''''''''''''''''''''''''''''''
If you have a large number of files, it might be useful to keep a local copy
of your container structure and listing. You can do this in a local
database, significantly reducing the chance of a naming conflict and
location of a specific object. By keeping a local copy of your container
structure, you can more easily update objects, if needed, without having
to list all your containers to discover which one contains the relevant object.
This can significantly reduce the preparation time required for updates.

Keeping a local database is most useful to customers using
Cloud Files for an object storage solution, since these are
frequently accessed programmatically and will also grow organically
over time. This also applies to any site that allows for
additional content, such as an uploads section, which may quickly
grow beyond expectations.

Pathing
~~~~~~~
Because containers, and their objects, do not nest, there are applications
which will fake a folder structure by adding a **path** to the beginning
of the object name.

For object storage, this enables better subdivision of slow growing,
closely-grouped data that you are unlikely to divide out again later.

For web acceleration, this enables pathing that displays in the
browser. For example, a pathed object named ``ducks/funny/duckling.jpg``
would become

.. code::

   http://c123456.r02.cf3.rackcdn.com/ducks/funny/duckling.jpg

.. TIP::
   You can use CNAME records to link your Cloud Files container to a
   branded URL that you display instead of a CDN URL. To learn more about
   CNAMEs, check out
   :how-to:`Using CNAMEs with Cloud Files containers <using-cnames-with-cloud-files-containers>`.

.. include:: /_common/seealso-concepts-cloud-files.txt
