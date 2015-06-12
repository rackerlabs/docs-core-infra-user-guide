Partslist for cross-references
==============================
Linking between pages in this guide requires use of reference IDs. 
A page without an ID cannot be linked to from another page. 

**Rules**

* Every content page must have an ID, 
  whether or not any other page currently links to it.

* When you create a content page, 
  check this list to confirm that the unique ID you imagine is unused, 
  then add the new ID to the list.

* Alphabetize the list by ID.

* ID must be unique within this guide, 
  http://rackspace-core-infra-user-guide.readthedocs.org/en/latest.

* Use "index" as the ID for the site-wide home page; 
  its source filename is index.rst;
  it generates published filename index.html.

* ID should match filename, unless matching the filename 
  violates the rule of uniqueness 
  (or is likely to violate the rule of uniqueness, 
  or some other rule of common sense, as the site expands).
  For example, 
  index.rst occurs in every directory, 
  so files named "index.rst" cannot all use "index" as their ID. 

* If ID cannot simply match the filename, 
  use elements of its directory structure to construct a unique
  and descriptive ID.
  "servicenet" is a descriptive ID; "page01" is not.
  
* If ID represents an anchor within the page rather than the 
  page itself, begin with the ID for the page and append 
  details to make it unique. 

----

**Use**

Begin every .rst page with a reference ID. 
After the reference ID: 
* a blank line  
* a line of delimiters 
* the section title
* a line of the same delimiters 
* on a new non-blank line, begin content 

Link to a page within the site by using its reference ID. 

* See examples at 
  https://sphinx-js-howto.readthedocs.org/en/latest/getting-started/linking-pages.html. 

----

**Inventory**

APIdirect                              = /cloud-interfaces/API/APIdirect.rst

assumptions                            = /cloud-guide-intro/assumptions.rst

backups                                = /cloud-preprod/backups.rst

base_images                            = /cloud-config/compute/cloud-images-product-concepts/base-images/index.rst

bestpractice                           = /cloud-ops/bestpractice.rst

block_storage                          = /cloud-config/storage/cloud-block-storageproduct_actions/block-storage.rst

boot                                   = /cloud-config/compute/cloud-servers-product-concepts/boot/index.rst

change_server                          = /cloud-config/compute/cloud-servers-product-concepts/change-server.rst

check_region_flavor_class              = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/check-region-flavor-class.rst

choose_flavor_class                    = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/choose-flavor-class.rst

cinder                                 = /cloud-interfaces/CLI/cinder.rst

cloud-config                           = /cloud-config/index.rst

cloud-config_compute                   = /cloud-config/compute/index.rst

cloud-config_network                   = /cloud-config/network/index.rst

cloud-config_storage                   = /cloud-config/storage/index.rst

cloud_block_storage_product_concepts   = /cloud-config/storage/cloud-block-storage-product-concepts/index.rst

cloud-guide-intro                      = /cloud-guide-intro/index.rst

cloud-images-product-actions           = /cloud-config/compute/cloud-images-product-actions/index.rst
 
cloud-images-product-concepts          = /cloud-config/compute/cloud-images-product-concepts/index.rst

cloud_images_sharing                   = /cloud-config/compute/cloud-images-product-concepts/sharing-images/index.rst

cloud-images-sharing-planning          = /cloud-config/compute/cloud-images-product-concepts/sharing-images/planning.rst

cloud-images-sharing-support           = /cloud-config/compute/cloud-images-product-concepts/sharing-images/support.rst

cloud_images_sharing_models            = /cloud-config/compute/cloud-images-product-concepts/sharing-images/models.rst

cloud-init_boot                        = /cloud-config/compute/cloud-servers-product-concepts/boot/cloud-init_boot.rst

cloud-interfaces                       = /cloud-interfaces/index.rst

cloud-interfaces_API                   = /cloud-interfaces/API/index.rst

cloud-interfaces_CLI                   = /cloud-interfaces/CLI/index.rst

cloud-interfaces_GUI                   = /cloud-interfaces/GUI/index.rst

cloud-intro                            = /cloud-intro/index.rst

cloud_networks_DNS                     = /cloud-config/network/cloud-networks-product-concepts/DNS.rst

cloud_networks_product_actions         = /cloud-config/network/cloud-networks-product-actions/index.rst

cloud_networks_product_concepts        = /cloud-config/network/cloud-networks-product-concepts/index.rst

cloudnetworks-benefits                 = /cloud-config/network/cloud-networks-product-concepts/cloudnetworks-benefits.rst

cloudnetworks-usecases                 = /cloud-config/network/cloud-networks-product-concepts/cloudnetworks-usecases.rst

cloud-ops                              = /cloud-ops/index.rst

cloud-preprod                          = /cloud-preprod/index.rst

cloud_servers_flavor_class             = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/index.rst

cloud_servers_metadata                 = /cloud-config/compute/cloud-servers-product-concepts/metadata/index.rst

cloud-servers-product-actions          = /cloud-config/compute/cloud-servers-product-actions/index.rst

cloud-servers-product-concepts         = /cloud-config/compute/cloud-servers-product-concepts/index.rst

cloud-tour                             = /cloud-intro/cloud-tour/index.rst

cloudblockstorage_API                  = /cloud-interfaces/API/cloudblockstorage-API.rst
cloudblockstorage_APIdemonstration     = /cloud-interfaces/API/cloudblockstorage-API.rst
cloudblockstorage_APIinvestigation     = /cloud-interfaces/API/cloudblockstorage-API.rst

cloudblockstorage_CLI                  = /cloud-interfaces/CLI/cloudblockstorage-CLI.rst

cloudblockstorage_GUI                  = /cloud-interfaces/GUI/cloudblockstorage-GUI.rst

cloudimages_API                        = /cloud-interfaces/API/cloudimages-API.rst
cloudimages_APIdemonstration           = /cloud-interfaces/API/cloudimages-API.rst
cloudimages_APIinvestigation           = /cloud-interfaces/API/cloudimages-API.rst

cloudimages_CLI                        = /cloud-interfaces/CLI/cloudimages-CLI.rst

cloudimages_GUI                        = /cloud-interfaces/GUI/cloudimages-GUI.rst

cloudnetworks_API                      = /cloud-interfaces/API/cloudnetworks-API.rst
cloudnetworks_APIdemonstration         = /cloud-interfaces/API/cloudnetworks-API.rst
cloudnetworks_APIinvestigation         = /cloud-interfaces/API/cloudnetworks-API.rst

cloudnetworks_CLI                      = /cloud-interfaces/CLI/cloudnetworks-CLI.rst

cloudnetworks_GUI                      = /cloud-interfaces/GUI/cloudnetworks-GUI.rst

cloudservers_API                       = /cloud-interfaces/API/cloudservers-API.rst
cloudservers_APIdemonstration          = /cloud-interfaces/API/cloudservers-API.rst
cloudservers_APIinvestigation          = /cloud-interfaces/API/cloudservers-API.rst

cloudservers_CLI                       = /cloud-interfaces/CLI/cloudservers-CLI.rst

cloudservers_GUI                       = /cloud-interfaces/GUI/cloudservers-GUI.rst

contactus                              = /cloud-guide-intro/contactus.rst

context                                = /cloud-intro/context.rst

core_infrastructure                    = /cloud-intro/core_infrastructure.rst

create_server                          = /cloud-config/compute/cloud-servers-product-concepts/create-server.rst

curl                                   = /cloud-interfaces/CLI/curl.rst

custom_images                          = /cloud-config/compute/cloud-images-product-concepts/custom-images.rst

customer_stories                       = /cloud-intro/customer-stories.rst

data_immutability                      = /cloud-config/compute/cloud-images-product-concepts/data-immutability.rst

default_base_images                    = /cloud-config/compute/cloud-images-product-concepts/base-images/default-base-images.rst

devopstools                            = /cloud-interfaces/API/devopstools.rst

disk_storage                           = /cloud-config/storage/cloud-block-storage-product-concepts/disk-storage.rst

diskconfig                             = /cloud-config/compute/cloud-servers-product-concepts/diskconfig.rst

document_history                       = /cloud-guide-intro/document-history.rst

drive_boot                             = /cloud-config/compute/cloud-servers-product-concepts/boot/drive-boot.rst

glance                                 = /cloud-interfaces/CLI/glance.rst

host_issues                            = /cloud-config/compute/cloud-servers-product-concepts/host-issues.rst

image_properties                       = /cloud-config/compute/cloud-images-product-concepts/image-properties.rst

import_export_images                   = /cloud-config/compute/cloud-images-product-concepts/import-export-images.rst

index                                  = index.rst (**home page for the site**)

lifecycle_base_images                  = /cloud-config/compute/cloud-images-product-concepts/base_images/lifecycle-base-images.rst

limits                                 = /cloud-ops/limits.rst

local_storage                          = /cloud-config/storage/cloud-block-storageproduct-concepts/local-storage.rst

monitoring                             = /cloud-preprod/monitoring.rst

moreinfo                               = /cloud-guide-intro/moreinfo.rst

moreinfo_API                           = /cloud-interfaces/API/moreinfo-API.rst

moreinfo_CLI                           = /cloud-interfaces/CLI/moreinfo-CLI.rst

moreinfo_GUI                           = /cloud-interfaces/GUI/moreinfo-GUI.rst

network_cloud_servers                  = /cloud-config/network/cloud-networks-product-concepts/network-cloud_servers.rst
network_cloud_servers-working          = /cloud-config/network/cloud-networks-product-concepts/network-cloud_servers.rst

network_onmetal_servers                = /cloud-config/network/cloud-networks-product-concepts/network-onmetal-servers.rst

network_rackconnect                    = /cloud-config/network/cloud-networks-product-concepts/network-rackconnect.rst

neutron                                = /cloud-interfaces/CLI/neutron.rst

nova                                   = /cloud-interfaces/CLI/nova.rst

nova-agent                             = /cloud-config/compute/cloud-servers-product-concepts/nova-agent.rst

on-demand_images                       = /cloud-config/compute/cloud-images-product-concepts/on-demand-images.rst

patching_base_images                   = /cloud-config/compute/cloud-images-product-concepts/base-images/patching-base-images.rst

personality_boot                       = /cloud-config/compute/cloud-servers-product-concepts/boot/personality-boot.rst

publicnet                              = /cloud-config/network/cloud-networks-product-concepts/publicnet.rst

scaling                                = /cloud-preprod/scaling.rst

SDK                                    = /cloud-interfaces/API/SDK.rst

security                               = /cloud-preprod/security.rst

scheduled_images                       = /cloud-config/compute/cloud-images-product-concepts/scheduled-images.rst

server_events                          = /cloud-config/compute/cloud-servers-product-concepts/server-events.rst

server_region                          = /cloud-config/compute/cloud-servers-product-concepts/server-region.rst

servicenet                             = /cloud-config/network/cloud-networks-product-concepts/servicenet.rst

set_metadata                           = /cloud-config/compute/cloud-servers-product-concepts/metadata/set-metadata.rst

setup_API                              = /cloud-interfaces/API/setup-API.rst

setup_CLI                              = /cloud-interfaces/CLI/setup-CLI.rst

setup_GUI                              = /cloud-interfaces/GUI/setup-GUI.rst

show_metadata                          = /cloud-config/compute/cloud-servers-product-concepts/metadata/show-metadata.rst

software_RAID                          = /cloud-config/storage/cloud-block-storage-product-concepts/software-RAID.rst

somethingnew                           = /cloud-ops/somethingnew.rst

SSH                                    = /cloud-config/compute/cloud-servers-product-concepts/SSH.rst

stack                                  = /cloud-preprod/stack.rst 

supernova                              = /cloud-interfaces/CLI/supernova.rst

support                                = /cloud-ops/support.rst

time                                   = /cloud-config/compute/cloud-servers-product-concepts/time.rst

tour_application_services              = /cloud-intro/cloud-tour/application-services.rst

tour_compute_services                  = /cloud-intro/cloud-tour/compute-services.rst

tour_data_services                     = /cloud-intro/cloud-tour/data-services.rst

tour_network_services                  = /cloud-intro/cloud-tour/network-services.rst

tour_storage_services                  = /cloud-intro/cloud-tour/storage-services.rst

tour_support_services                  = /cloud-intro/cloud-tour/support-services.rst

troubleshoot                           = /cloud-ops/troubleshoot.rst

virtualization_modes                   = /cloud-config/compute/cloud-images-product-concepts/virtualization_modes.rst

