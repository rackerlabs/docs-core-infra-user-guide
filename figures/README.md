Figures for Rackspace Cloud Core Infrastructure Services User Guide
===================================================================
This directory contains *figures* used anywhere in 
http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/. 

A figure is a kind of image.

Figures are drawings related to an idea discussed 
in the text. The drawings show how things work conceptually but 
not procedurally. Figures visually explain a concept.

Procedural demonstrations are in another directory,  
named *screenshots* because they show how a Cloud Control Panel 
session looks. Screenshots visually demonstrate a process.

----
To include a figure in the guide:

* Save the publishable figure (for example, .png or .svg) 
  in this *figures* directory 
  with a descriptive filename. "CloudServersArchitecture" 
  is a descriptive filename; "Image01" is not.
  
* If you have a source drawing for the publishable figure 
  (for example, .vsdx (Visio) or .graffle (OmniGraffle)), 
  save the source drawing 
  in this *figures* directory 
  with a descriptive filename that matches it to the 
  publishable figure.
  For example, "NetworkLayout.vsdx" is recognizable as the source 
  of "NetworkLayout.png". 
  
* On the page where you intend the image to appear, 
  at the location where you intend it to appear, 
  call for it with the full path to the publishable figure's filename, 
  providing descriptive alternate text 
  so non-visual browsers can summarize its meaning. 
  Follow this model:

```
  .. image:: ../../../figures/ExampleImageFileName.png
   :alt: Virtual Cloud Servers are the core of a rich configuration.
```

* Update the inventory (below), connecting the image to 
  its intended use, its source, and at least one human 
  responsible for it. 
  Keep the inventory alphabetized by filename.

| image filename                       | used at                                                     | origin                                       | date         | added by             |
| (in this directory)                  | (in published guide)                                        | (clue: URL,source filename,creator's name)   | (yyyy-mm-dd) | (contributor's name) |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
| CloudImagesHandshaking.png           | /cloud_config/compute/                                      | http://docs.rackspace.com/images/api/v2/     |              |                      |
|                                      | cloud_images_product_concepts/sharing_images/models.html    | ci-gettingstarted/content/image-sharing.html | 2015-03-01   | Cat Lookabaugh       |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
| CloudServerNetworkRemovalResults.png | /cloud_config/network/                                      | https://github.com/rackerlabs/               | 2014-07-22   | Sameer Satyam        |
|                                      | cloud_networks_product_concepts/network_cloud_servers.html  | docs-core-infra-user-guide/issues/26         |              |                      |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
| CloudServerOnMetalArchitecture.png   | /cloud_intro/core_infrastructure.html                       | internal ProductWeb                          | 2015-03-01   | Rose Coste           |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
| CloudServerVirtualArchitecture.png   | /cloud_intro/core_infrastructure.html                       | internal ProductWeb                          | 2015-03-01   | Rose Coste           |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
| ManagedCloud.png                     | /cloud_config/compute/                                      | http://www.rackspace.co.uk/cloud/servers     | 2015-03-01   | Rose Coste           |
|                                      | cloud_servers_product_concepts/index.html                   |                                              |              |                      |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
| RackConnectEnterpriseConfig.jpg      | /cloud_config/network/                                      | internal ProductWeb                          | 2015-03-01   | Rose Coste           |
|                                      | cloud_networks_product_concepts/network_rackconnect.html    |                                              |              |                      |
| ------------------------------------ | ----------------------------------------------------------- | -------------------------------------------- | ------------ | -------------------- |
