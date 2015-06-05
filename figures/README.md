Figures for Rackspace Cloud Core Infrastructure Services User Guide
===================================================================
All figures are now in the _images directory for building.

This document describes figures in this context. A figure is a kind of image.

Figures are drawings related to an idea discussed 
in the text. The drawings show how things work conceptually but 
not procedurally. Figures visually explain a concept.

Procedural demonstrations are in another directory,  
named *screenshots* because they show how a Cloud Control Panel 
session looks. Screenshots visually demonstrate a process.

----
To include a figure in the guide:

* Save the publishable figure (for example, .png or .svg) 
  in the */_images/* directory 
  with a descriptive filename. "CloudServersArchitecture" 
  is a descriptive filename; "Image01" is not.
  
* If you have a source drawing for the publishable figure 
  (for example, .vsdx (Visio) or .graffle (OmniGraffle)), 
  save the source drawing 
  in the */_images/* directory 
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
  .. figure:: /_images/ExampleImageFileName.png
     :alt: Cloud Servers are awesome.
           If I say more than one line, 
           I indent.
           
     *A caption is italicized below the figure*
```

* Update the inventory (below), connecting the image to 
  its intended use, its source, and at least one human 
  responsible for it. 
  Keep the inventory alphabetized by filename.

----
**Inventory of figures**

* **CloudImagesHandshaking.png**
  * used at /cloud_config/compute/cloud_images_product_concepts/sharing_images/models.html
  * originated from http://docs.rackspace.com/images/api/v2/ci-gettingstarted/content/image-sharing.html 
  * collection date 2015-03-01
  * contributed by Cat Lookabaugh

* **CloudServerNetworkRemovalResults.png**
  * used at /cloud_config/network/cloud_networks_product_concepts/network_cloud_servers.html
  * originated from https://github.com/rackerlabs/docs-core-infra-user-guide/issues/26 
  * collection date 2014-07-22
  * contributed by Sameer Satyam
  
* **CloudServerOnMetalArchitecture.png**
  * used at /cloud_config/compute/cloud_servers_product_concepts/index.html
  * collection date 2015-03-01
  * contributed by Rose Coste

* **CloudServerVirtualArchitecture.png**
  * used at /cloud_config/compute/cloud_servers_product_concepts/index.html
  * originated from internal ProductWeb
  * collection date 2015-03-01
  * contributed by Rose Coste
  
* **core-infrastructure.png**
  * used at /cloud_intro/core_infrastructure.html
  * source here, in /figures/core-infrastructure.xml; 
    to change the drawing, open the XML in https://www.draw.io/, 
    then export a new .PNG and save it here
  * collection date 2015-06-04
  * contributed by Nate Archer

* **RackConnectEnterpriseConfig.jpg**
  * used at /cloud_config/network/cloud_networks_product_concepts/network_rackconnect.html
  * originated from internal ProductWeb
  * collection date 2015-03-01
  * contributed by Rose Coste
  
