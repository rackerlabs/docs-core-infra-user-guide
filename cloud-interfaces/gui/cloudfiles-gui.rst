.. _cloudfiles-gui:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Cloud Files and the Cloud Control Panel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The Cloud Control Panel groups the core infrastructure services
as described at :ref:`cloud-tour`,
with
Cloud Files (labeled **Files**)
available
under **Storage**.

# make sure to put an image here similar to the CBS image

You can use the Cloud Control Panel to help you
observe and manage your Cloud Block Storage configuration.
For ideas about what to do first,
visit
:kc-article:`Cloud Files overview <cloud-files-overview>`.

Create a Container
''''''''''''''''''
To create a new container, log into the :mycloud:`Cloud Control Panel<>`.
In the top navigation bar, select **Storage > Files** and click
**Create Container**.

# image here to show create container button and options

Name the container, choose a region,  and select the type:
Private, Public (Enabled CDN), or Static Website.

* Private containers allow you to securely store data on the cloud and
  access it through the Control Panel or API.
* Public (Enabled CDN) containers automatically store files on
  servers close to your users, which speeds up the delivery of your
  data.
* A container can also host a static website. Upload an html file
  named **index.html** to set up as your index page. Add a domain name
  by going to your domain hose and setting up a CNAME to your CDN URL.
  For more information on hosting static websites, try
  :kc-article:`Serve Static Content for Websites by Using Cloud Files
  <serve-static-content-for-websites-by-using-cloud-files>`.

Upload Files to the Container
'''''''''''''''''''''''''''''
To upload files to one of your containers, first log into the
:mycloud:`Cloud Control Panel <>`. In the top navigation bar, select
**Storage > Files** and click on the name of the container to which
you want to upload files.

Click **Upload Files**, select the files to upload, and then click **Open**.
After the file is uploaded, click **Close Window**. The file will
then appear in the list of available files within the container.
Click the gear icon next to your file and select **View All Links**
to see the options for sharing your file.

# image to show uploading files to container
