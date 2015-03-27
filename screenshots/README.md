Screenshots for Rackspace Cloud Core Infrastructure Services User Guide
=======================================================================
This directory contains *screenshots* used anywhere in 
http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/. 

A screenshot is a kind of image.

Screenshots show how a Cloud Control Panel 
session looks. Screenshots visually demonstrate a process.

Drawings are in another directory, 
named *figures*. The drawings show how things work conceptually but 
not procedurally. Figures visually explain a concept.

----
To include a screenshot in the guide:

* Save the screenshot (probably of type .png) 
  in this *screenshots* directory 
  with a descriptive filename. "CloudServerCreation" 
  is a descriptive filename; "Image01" is not.
  
* On the page where you intend the image to appear, 
  at the location where you intend it to appear, 
  call for it with the full path to the screenshot's filename, 
  providing descriptive alternate text 
  so non-visual browsers can summarize its meaning. 
  Follow this model:

```
  .. image:: ../../../screenshots/ExampleProcess.png
     :alt: Cloud Servers are awesome.
           If I say more than one line, 
           I indent.
```

* Update the inventory (below), connecting the image to 
  its intended use, its source, and at least one human 
  responsible for it. 
  Keep the inventory alphabetized by filename.

----
**Inventory of screenshots**

* **CloudDNSAddReverse.png** 
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/network/cloud_networks_product_concepts/DNS.html
  * collected from http://www.rackspace.com/knowledge_center/article/create-a-reverse-dns-record-0 
  * collection date 2015-03-01 (KC article dated 2015-02-02)
  * contributed by Rose Coste (KC article author listed as "Rackspace Support")
  
* **CloudDNSAddReverseDetails.png** 
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/network/cloud_networks_product_concepts/DNS.html
  * collected from http://www.rackspace.com/knowledge_center/article/create-a-reverse-dns-record-0 
  * collection date 2015-03-01 (KC article dated 2015-02-02)
  * contributed by Rose Coste (KC article author listed as "Rackspace Support")
  
* **CloudDNSCreateDomain.png** 
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/network/cloud_networks_product_concepts/DNS.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01 
  * contributed by Rose Coste
  
  * **CloudOrchestrationRailsFlavors.png**
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_preprod/stack.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-26
  * contributed by Rose Coste
  
* **CloudServerCreateFlavorStandardInstance.png**
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/compute/cloud_servers_product_concepts/server_region.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste
  
* **CloudServerCreateImageUbuntu.png**
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/compute/cloud_servers_product_concepts/server_region.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste 

* **CloudServerCreateOnMetal.png** xxxxxxxx
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/compute/cloud_servers_product_concepts/flavor_class/index.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste
  
* **CloudServerCreateRegionDFW.png**
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/compute/cloud_servers_product_concepts/server_region.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste  
  
* **CloudServerCreateVirtual.png** xxxxxxxx
  * used at http://rackspace-core-infra-user-guide.readthedocs.org/en/latest/cloud_config/compute/cloud_servers_product_concepts/flavor_class/index.html
  * collected from https://mycloud.rackspace.com/ 
  * collection date 2015-03-01
  * contributed by Rose Coste

