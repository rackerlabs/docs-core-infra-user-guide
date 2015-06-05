Screenshots for Rackspace Cloud Core Infrastructure Services User Guide
=======================================================================
All screenshots are now in the _images directory for building.

This document describes screenshots in this context. A screenshot is a kind of
image.

Screenshots show how a Cloud Control Panel session looks. Screenshots visually
demonstrate a process.

Drawings are also in the *_images* directory. The drawings show how things
work conceptually but not procedurally. Figures visually explain a concept.

----
To include a screenshot in the guide:

* Save the screenshot (probably of type .png) 
  in the *_images* directory 
  with a descriptive filename. "CloudServerCreation" 
  is a descriptive filename; "Image01" is not.

* On the page where you intend the image to appear, 
  at the location where you intend it to appear, 
  call for it with the full path to the screenshot's filename, 
  providing descriptive alternate text 
  so non-visual browsers can summarize its meaning. 
  Follow this model:

```
  .. figure:: /_images/screenshots/ExampleProcess.png
     :alt: Cloud Servers are awesome.
           If I say more than one line, 
           I indent.
           
     *Italicize a caption explaining the screenshot.*
```

Although we're collecting screenshots and figures separately, 
we have to use the "figures" directive to publish them all
since that is the only way to provide a caption.

* Update the inventory (below), connecting the image to 
  its intended use, its source, and at least one human 
  responsible for it.
  Keep the inventory alphabetized by filename.

----
**Inventory of screenshots**

* **AccountResourceLimits.png** 
  * used at /cloud_interfaces/GUI/index.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-18
  * contributed by Rose Coste

* **ChromeViewDeveloper.png** 
  * used at /cloud_interfaces/API/cloudservers_API.html
  * used at /cloud_interfaces/API/cloudnetworks_API.html
  * used at /cloud_interfaces/API/cloudimages_API.html
  * used at /cloud_interfaces/API/cloudblockstorage_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-15
  * contributed by Rose Coste
  
* **CloudBigData0clusters.png** 
  * used at /cloud_ops/somethingnew.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-19 
  * contributed by Rose Coste

* **CloudBlockStorage0volumes.png** 
  * used at /cloud_interfaces/API/cloudblockstorage_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-04-30
  * contributed by Rose Coste
  
* **CloudBlockStorage1volume.png** 
  * used at /cloud_interfaces/API/cloudblockstorage_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-04-30
  * contributed by Rose Coste
  
 * **CloudBlockStorageListVolumesGET.png** 
  * used at /cloud_interfaces/API/cloudblockstorage_API.html
  * collected from http://api.rackspace.com/ 
  * collection date 2015-04-30
  * contributed by Rose Coste 

* **CloudBlockStorageSDKPHP.png** 
  * used at /cloud_interfaces/API/cloudblockstorage_API.html
  * collected from https://developer.rackspace.com/docs/cloud-block-storage/getting-started/ 
  * collection date 2015-04-30
  * contributed by Rose Coste

* **CloudDNSAddReverse.png** 
  * used at /cloud_config/network/cloud_networks_product_concepts/DNS.html
  * collected from http://www.rackspace.com/knowledge_center/article/create-a-reverse-dns-record-0 
  * collection date 2015-03-01 (KC article dated 2015-02-02)
  * contributed by Rose Coste (KC article author listed as "Rackspace Support")
  
* **CloudDNSAddReverseDetails.png** 
  * used at /cloud_config/network/cloud_networks_product_concepts/DNS.html
  * collected from http://www.rackspace.com/knowledge_center/article/create-a-reverse-dns-record-0 
  * collection date 2015-03-01 (KC article dated 2015-02-02)
  * contributed by Rose Coste (KC article author listed as "Rackspace Support")
  
* **CloudDNSCreateDomain.png** 
  * used at /cloud_config/network/cloud_networks_product_concepts/DNS.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01 
  * contributed by Rose Coste
  
* **CloudImagesListAll.png** 
  * used at /cloud_interfaces/API/cloudimages_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-11
  * contributed by Rose Coste 
  
* **CloudImagesListImagesGET.png** 
  * used at /cloud_interfaces/API/cloudimages_API.html
  * collected from http://api.rackspace.com/ 
  * collection date 2015-05-11
  * contributed by Rose Coste 
  
* **CloudImagesSDKpython.png** 
  * used at /cloud_interfaces/API/cloudimages_API.html
  * collected from https://developer.rackspace.com/docs/cloud-images/getting-started/ 
  * collection date 2015-05-11
  * contributed by Rose Coste 
  
* **CloudNetworksListAll.png** 
  * used at /cloud_interfaces/API/cloudnetworks_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-07
  * contributed by Rose Coste 
  
* **CloudNetworksListNetworksGET.png** 
  * used at /cloud_interfaces/API/cloudnetworks_API.html
  * collected from http://api.rackspace.com/ 
  * collection date 2015-05-07
  * contributed by Rose Coste 
  
* **CloudNetworksSDKjava.png** 
  * used at /cloud_interfaces/API/cloudnetworks_API.html
  * collected from https://developer.rackspace.com/docs/cloud-networks/getting-started/ 
  * collection date 2015-05-07
  * contributed by Rose Coste 
  
* **CloudOrchestrationRailsFlavors.png**
  * used at /cloud_preprod/stack.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-26
  * contributed by Rose Coste
  
* **CloudServerCreateFlavorStandardInstance.png**
  * used at /cloud_config/compute/cloud_servers_product_concepts/server_region.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste
  
* **CloudServerCreateImageUbuntu.png**
  * used at /cloud_config/compute/cloud_servers_product_concepts/server_region.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste 

* **CloudServerCreateOnMetal.png** 
  * used at /cloud_config/compute/cloud_servers_product_concepts/flavor_class/index.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste
  
* **CloudServerCreateRegionDFW.png**
  * used at /cloud_config/compute/cloud_servers_product_concepts/server_region.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste  
  
* **CloudServerCreateVirtual.png** 
  * used at /cloud_config/compute/cloud_servers_product_concepts/flavor_class/index.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste
  
* **CloudServersListAll.png** 
  * used at /cloud_interfaces/API/cloudservers_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-04-28
  * contributed by Rose Coste
  
* **CloudServersListServersGET.png** 
  * used at /cloud_interfaces/API/cloudservers_API.html
  * collected from http://api.rackspace.com/ 
  * collection date 2015-04-29
  * contributed by Rose Coste

* **CloudServersSDKpython.png** 
  * used at /cloud_interfaces/API/cloudservers_API.html
  * collected from https://developer.rackspace.com/docs/cloud-servers/getting-started/ 
  * collection date 2015-04-28
  * contributed by Rose Coste

* **CreateTicketServersResourceLimit.png** 
  * used at /cloud_interfaces/GUI/index.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-18
  * contributed by Rose Coste

* **NetworkingGroup.png** 
  * used at /cloud_interfaces/GUI/cloudnetworks_GUI.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-13
  * contributed by Rose Coste
  
* **NetworkingNetworks.png** 
  * used at /cloud_interfaces/API/cloudnetworks_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-07
  * contributed by Rose Coste  
  
* **quickstart-shell.png** 
  * used at /cloud_interfaces/CLI/curl.html
  * collected from https://developer.rackspace.com/docs/cloud-block-storage/getting-started/ 
  * collection date 2015-05-26
  * contributed by Rose Coste
  
* **ReleaseNotesFeed-API.png** 
  * used at /cloud_interfaces/API/moreinfo_API.html
  * collected from http://docs.rackspace.com/cbs/api/v1.0/cbs-releasenotes/ 
  * collection date 2015-05-19
  * contributed by Rose Coste 

* **ReleaseNotesFeed-SDK.png** 
  * used at /cloud_interfaces/API/moreinfo_API.html
  * collected from https://developer.rackspace.com/sdks/ 
  * collection date 2015-05-19
  * contributed by Rose Coste 

* **ServersGroup.png** 
  * used at /cloud_interfaces/API/cloudimages_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-12
  * contributed by Rose Coste 
  
* **ServersSavedImages.png** 
  * used at /cloud_interfaces/GUI/cloudservers_GUI.html
  * used at /cloud_interfaces/GUI/cloudimages_GUI.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-12
  * contributed by Rose Coste 
  
* **StorageGroup.png** 
  * used at /cloud_interfaces/GUI/cloudblockstorage_GUI.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-05-13
  * contributed by Rose Coste

* **StorageBlockStorageVolumes.png** 
  * used at /cloud_interfaces/API/cloudblockstorage_API.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-04-30
  * contributed by Rose Coste
