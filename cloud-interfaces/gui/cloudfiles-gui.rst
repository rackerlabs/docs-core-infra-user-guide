.. _cloudfiles-gui:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud Files and the Cloud Control Panel
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The Cloud Control Panel groups the core infrastructure services
as described in :ref:`cloud-tour`,
with
Cloud Files (labeled **Files**)
available
under **Storage**.

.. figure:: /_images/controlpanelcloudfiles.png
   :scale: 80%
   :alt: The Storage group includes Cloud Files.

   *The Storage group includes Cloud Files.*

You can use the Cloud Control Panel to help you
observe and manage your Cloud Files configuration.
For ideas about what to do first,
visit
:how-to:`Cloud Files overview <cloud-files-overview>`.

Create a Container
''''''''''''''''''
To create a new container, log in to the :mycloud:`Cloud Control Panel<>`.
In the top navigation bar, select **Storage > Files** and click
**Create Container**.

.. figure:: /_images/cloudfilescreatecontainer.png
   :scale: 80%
   :alt: To create a container, enter a name, choose a region, and
         select the type.

   *To create a container, enter a name, choose a region, and
   select the type: Private, Public (Enabled CDN), or Static
   Website.*

* Private containers enable you to securely store data on the cloud and
  access it through the Cloud Control Panel or API.
* Public (Enabled CDN) containers automatically store files on
  servers close to your users, which speeds up the delivery of your
  data.
* A container can also host a static website. Upload an html file
  named **index.html** to set up as your index page. Add a domain name
  by going to your domain hose and setting up a CNAME to your CDN URL.
  For more information on hosting static websites, try
  :how-to:`Serve Static Content for Websites by Using Cloud Files
  <serve-static-content-for-websites-by-using-cloud-files>`.

Upload Files to the Container
'''''''''''''''''''''''''''''
To upload files to one of your containers, first log in to the
:mycloud:`Cloud Control Panel <>`. In the top navigation bar, select
**Storage > Files** and click on the name of the container to which
you want to upload files.

.. figure:: /_images/cloudfilesuploadfile.png
   :scale: 80%
   :alt: If you have no Cloud files objects, the Cloud Control Panel
         shows you how to upload one.

   *If you have no Cloud Files objects, the Cloud Control Panel
   shows you how to upload one.*
