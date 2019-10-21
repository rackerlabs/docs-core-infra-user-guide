Images for Rackspace Cloud Core Infrastructure Services User Guide
=======================================================================
All images must reside in this *_images* directory.

"All images" includes:

* Figures

Figures are drawings related to an idea discussed
in the text. The drawings show how things work conceptually but
not procedurally. Figures visually explain a concept.

*Use the figure directive to include figures;
give each figure alternate text and a caption.*

* Logos

Logos represent a single word or phrase such as the
the name of a product

*Use the image directive to include logos;
give each logo alternate text.*

* Screenshots

Screenshots show how a Cloud Control Panel session looks.
Screenshots visually demonstrate a process
or a portion of a process.

*Use the figure directive to include screenshots;
give each screenshot alternate text and a caption.*

For everything stored in *_images*,
use this *README* to maintain an inventory describing what we have,
where we got it, and how we use it.


----
To include any image in the guide:

* Save the image (probably of type .png)
  in the *_images* directory
  with a descriptive filename. "CloudServerCreation"
  is a descriptive filename; "Image01" is not.

* On the page where you intend the image to appear,
  at the location where you intend it to appear,
  call for it from ``/_images/`` followed by its filename,
  providing descriptive alternate text
  so non-visual browsers can verbally summarize its meaning.

  If the image is a figure or a screenshot,
  also provide an italicized caption.
  Follow this model:

```
  .. figure:: /_images/screenshots/ExampleProcess.png
     :alt: Cloud Servers are awesome.
           If I say more than one line,
           I indent.

     *Italicize a caption explaining the screenshot.*
```

* Update the inventory (below), connecting the image to
  its intended use, its age, its source, and at least one human
  responsible for it.
  Keep the inventory grouped by image type
  (figures, logos, screenshots)
  and alphabetized by filename within image type.

----
**Inventory of figures**

* **cloudfilesinterfaces.png**
  * used at
  * source here, in cloudfilesinterfaces.xml
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-07-10
  * contributed by Nate Archer

* **cloudimageshandshaking.png**
  * used at /cloud-config/compute/cloud-images-product-concepts/sharing-images/models.html
  * source here, in cloudimageshandshaking.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-09
  * contributed by Nate Archer

* **cloudimagesharing.png**
  * used at cloud-config/compute/cloud-images-product-concepts/sharing-images/models.html
  * source here, in cloudimagesharing.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-15
  * contributed by Nate Archer

* **cloudservernetworkremovalresults.png**
  * used at /cloud-config/network/cloud-networks-product-concepts/servicenet-publicnet-requirement.html
  * source here, in cloudservernetworkremovalresults.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-08
  * contributed by Nate Archer

* **cloudserveronmetalarchitecture.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/index.html
  * source here, in cloudserveronmetalarchitecture.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-05
  * contributed by Nate Archer

* **cloudservervirtualarchitecture.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/index.html
  * source here, in cloudservervirtualarchitecture.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-05
  * contributed by Nate Archer

* **core-infrastructure.png**
  * used at /cloud-intro/core-infrastructure.html
  * source here, in core-infrastructure.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-04
  * contributed by Nate Archer

* **rackconnectenterpriseconfig.png**
  * used at /cloud-config/network/cloud-networks-product-concepts/network-rackconnect.html
  * source here, in rackconnectenterpriseconfig.xml;
    to change the drawing, open the XML in https://www.draw.io/,
    then export a new .PNG and save it here
  * collection date 2015-06-12
  * contributed by Nate Archer


----
**Inventory of logos**

* **logo-autoscale-50x50.png**
  * used at /cloud-intro/cloud-tour/application-services.html
  * original size here, logo-autoscale.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudbigdata-50x50.png**
  * used at /cloud-intro/cloud-tour/data-services.html
  * original size here, logo-cloudbigdata.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudbackup-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/storage-services.html
  * original size here, logo-cloudbackup.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudblockstorage-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/storage-services.html
  * original size here, logo-cloudblockstorage.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudcdn-50x50.png**
  * used at /cloud-intro/cloud-tour/storage-services.html
  * resized to 50px x 50px with inkscape editor
  * collection date 2015-06-25
  * original from Margaret Eker, resized by Margaret Eker

* **logo-clouddatabases-50x50.png**
  * used at /cloud-intro/cloud-tour/data-services.html
  * original size here, logo-clouddatabases.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-clouddns-50x50.png**
  * used at /cloud-intro/cloud-tour/network-services.html
  * original size here, logo-clouddns.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudfeeds-50x50.png**
  * used at /cloud-intro/cloud-tour/support-services.html
  * original size here, logo-cloudfeeds.png;
    resized to 64px x 50px with PhotoScape
  * collection date 2015-08-11
  * original from Peter Kazmir, resized by Stephanie Fillmon

* **logo-cloudfiles-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/storage-services.html
  * original size here, logo-cloudfiles.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudidentity-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/support-services.html
  * original size here, logo-cloudidentity.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudimages-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/compute-services.html
  * original size here, logo-cloudimages.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudloadbalancers-50x50.png**
  * used at /cloud-intro/cloud-tour/network-services.html
  * original size here, logo-cloudloadbalancers.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudmetrics-50x50.png**
  * used at /cloud-intro/cloud-tour/application-services.html
  * resized to 50px x 50px with inkscape editor
  * collection date 2015-06-25
  * original from Margaret Eker, resized by Margaret Eker

* **logo-cloudmonitoring-50x50.png**
  * used at /cloud-intro/cloud-tour/application-services.html
  * original size here, logo-cloudmonitoring.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudnetworks-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/network-services.html
  * original size here, logo-cloudnetworks.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudorchestration-50x50.png**
  * used at /cloud-intro/cloud-tour/application-services.html
  * original size here, logo-cloudorchestration.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-cloudservers-50x50.png**
  * used at /index.html
  * used at /cloud-intro/cloud-tour/compute-services.html
  * original size here, logo-cloudservers.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-objectrocket-50x50.png**
  * used at /cloud-intro/cloud-tour/data-services.html
  * original size 156x54;
    resized to 154px x 50px with SnagIt Editor
  * collection date 2015-06-29
  * SnagIt from http://objectrocket.com/features by Rose Coste

* **logo-rackconnect-50x50.png**
  * used at /cloud-intro/cloud-tour/network-services.html
  * original size here, logo-rackconnect.png;
    resized to 50px x 50px with SnagIt Editor
  * collection date 2015-06-07
  * original from Lane Fielder, resized by Rose Coste

* **logo-rackspaceintelligence-50x50.png**
  * used at /cloud-intro/cloud-tour/application-services.html
  * original size here, logo-rackspaceintelligence.png;
    resized to 64px x 50px with PhotoScape
  * collection date 2015-08-11
  * original from Constanze Kratel, resized by Stephanie Fillmon

----
**Inventory of screenshots**

* **autoscale-nogroups.png**
  * used at /cloud-preprod/network-ssh.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-12-24
  * contributed by Rose Coste

* **accountresourcelimits.png**
  * used at /cloud-interfaces/gui/index.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-18
  * contributed by Rose Coste

* **chromeviewdeveloper.png**
  * used at /cloud-interfaces/api/cloudservers-api.html
  * used at /cloud-interfaces/api/cloudnetworks-api.html
  * used at /cloud-interfaces/api/cloudimages-api.html
  * used at /cloud-interfaces/api/cloudblockstorage-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-15
  * contributed by Rose Coste

* **cloudbigdata0clusters.png**
  * used at /cloud-ops/somethingnew.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-19
  * contributed by Rose Coste

* **cloudblockstorage0volumes.png**
  * used at /cloud-interfaces/api/cloud.rackspace.com/
  * collection date 2015-04-30
  * contributed by Rose Coste

* **cloudblockstorage1volume.png**
  * used at /cloud-interfaces/api/cloudblockstorage-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-04-30
  * contributed by Rose Coste

* **cloudblockstoragesdkphp.png**
  * used at /cloud-interfaces/api/cloudblockstorage-api.html
  * collected from https://developer.rackspace.com/docs/cloud-block-storage/getting-started/
  * collection date 2015-04-30
  * contributed by Rose Coste

* **clouddnsaddreverse.png**
  * used at /cloud-config/network/cloud-networks-product-concepts/dns.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-06-16
  * contributed by Rose Coste

* **clouddnsaddreversedetails.png**
  * used at /cloud-config/network/cloud-networks-product-concepts/dns.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-06-16
  * contributed by Rose Coste

* **clouddnscreatedomain.png**
  * used at /cloud-config/network/cloud-networks-product-concepts/dns.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-01
  * contributed by Rose Coste

* **cloudfilescreatecontainer.png**
  * used at /cloud-interfaces/gui/cloudfiles-gui.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **cloudfilescreatecontainerbase.png**
  * undecorated, base image for cloudfilescreatecontainer.png
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **cloudfilessdk.png**
  * undecorated, base image for cloudfilessdkphp.png
  * collected from https://developer.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **cloudfilessdkphp.png**
  * used at /cloud-interfaces/api/cloudfiles-api.html
  * collected from https://developer.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **cloudfilesuploadfile.png**
  * used at /cloud-interfaces/gui/cloudfiles-gui.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **cloudimageslistall.png**
  * used at /cloud-interfaces/api/cloudimages-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-11
  * contributed by Rose Coste

* **cloudimagessdkpython.png**
  * used at /cloud-interfaces/api/cloudimages-api.html
  * collected from https://developer.rackspace.com/docs/cloud-images/getting-started/
  * collection date 2015-05-11
  * contributed by Rose Coste

* **cloudnetworkslistall.png**
  * used at /cloud-interfaces/api/cloudnetworks-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-07
  * contributed by Rose Coste

* **cloudnetworkssdkjava.png**
  * used at /cloud-interfaces/api/cloudnetworks-api.html
  * collected from https://developer.rackspace.com/docs/cloud-networks/getting-started/
  * collection date 2015-05-07
  * contributed by Rose Coste

* **cloudorchestrationrailsflavors.png**
  * used at /cloud-preprod/stack.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-26
  * contributed by Rose Coste

* **cloudservercreateflavorstandardinstance.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/server-region.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-01
  * contributed by Rose Coste

* **cloudservercreateimageubuntu.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/server-region.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-01
  * contributed by Rose Coste

* **cloudservercreateonmetal.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/flavor-class/index.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-01
  * contributed by Rose Coste

* **cloudservercreateregiondfw.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/flavor-class/check-region-flavor-class.html
  * used at /cloud-config/compute/cloud-servers-product-concepts/server-region.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-01
  * contributed by Rose Coste

* **cloudservercreatevirtual.png**
  * used at /cloud-config/compute/cloud-servers-product-concepts/flavor-class/index.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-03-01
  * contributed by Rose Coste

* **cloudserverslistall.png**
  * used at /cloud-interfaces/api/cloudservers-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-04-28
  * contributed by Rose Coste

* **cloudserverssdkpython.png**
  * used at /cloud-interfaces/api/cloudservers-api.html
  * collected from https://developer.rackspace.com/docs/cloud-servers/getting-started/
  * collection date 2015-04-28
  * contributed by Rose Coste

* **createticketserversresourcelimit.png**
  * used at /cloud-interfaces/gui/index.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-18
  * contributed by Rose Coste

* **controlpanelcloudfiles.png**
  * used at /cloud-interfaces/api/cloudfiles-api.html
  * used at /cloud-interfaces/gui/cloudfiles-gui.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **controlpanelstorage**
  * undecorated, base image for controlpanelcloudfiles.png
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-07-23
  * contributed by Stephanie Fillmon

* **flavorclass-network-speed.png**
  * used at /cloud-config/network/cloud-networks-product-concepts/network-cloud-servers.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-06-16
  * contributed by Rose Coste

* **networkinggroup.png**
  * used at /cloud-interfaces/gui/cloudnetworks-gui.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-13
  * contributed by Rose Coste

* **networkingnetworks.png**
  * used at /cloud-interfaces/api/cloudnetworks-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-07
  * contributed by Rose Coste

* **quickstart-shell.png**
  * used at /cloud-interfaces/cli/curl.html
  * collected from https://developer.rackspace.com/docs/cloud-block-storage/getting-started/
  * collection date 2015-05-26
  * contributed by Rose Coste

* **releasenotesfeed-api.png**
  * used at /cloud-interfaces/api/moreinfo-api.html
  * collected from https://docs.rackspace.com/cbs/api/v1.0/cbs-releasenotes/
  * collection date 2015-05-19
  * contributed by Rose Coste

* **releasenotesfeed-SDK.png**
  * used at /cloud-interfaces/api/moreinfo-api.html
  * collected from https://developer.rackspace.com/sdks/
  * collection date 2015-05-19
  * contributed by Rose Coste

* **serversgroup.png**
  * used at /cloud-interfaces/api/cloudimages-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-12
  * contributed by Rose Coste

* **serverssavedimages.png**
  * used at /cloud-interfaces/gui/cloudservers-gui.html
  * used at /cloud-interfaces/gui/cloudimages-gui.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-12
  * contributed by Rose Coste

* **status-disruption-cloudservers.png**
  * used at /cloud-ops/troubleshoot.html
  * collected from https://status.rackspace.com/
  * collection date 2015-12-29
  * contributed by Rose Coste

* **status-disruption-cloudservers-detail.png**
  * used at /cloud-ops/troubleshoot.html
  * collected from https://status.rackspace.com/
  * collection date 2015-12-29
  * contributed by Rose Coste

* **storagegroup.png**
  * used at /cloud-interfaces/gui/cloudblockstorage-gui.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-05-13
  * contributed by Rose Coste

* **storageblockstoragevolumes.png**
  * used at /cloud-interfaces/api/cloudblockstorage-api.html
  * collected from https://mycloud.rackspace.com/
  * collection date 2015-04-30
  * contributed by Rose Coste
