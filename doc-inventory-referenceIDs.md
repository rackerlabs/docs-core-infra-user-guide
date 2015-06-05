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

APIdirect                              = /cloud_interfaces/API/APIdirect.rst

assumptions                            = /cloud_guide_intro/assumptions.rst

backups                                = /cloud_preprod/backups.rst

base_images                            = /cloud_config/compute/cloud_images_product_concepts/base_images/index.rst

bestpractice                           = /cloud_ops/bestpractice.rst

block_storage                          = /cloud_config/storage/cloud_block_storage_product_actions/block_storage.rst

boot                                   = /cloud_config/compute/cloud_servers_product_concepts/boot/index.rst

change_server                          = /cloud_config/compute/cloud_servers_product_concepts/change_server.rst

check_region_flavor_class              = /cloud_config/compute/cloud_servers_product_concepts/flavor_class/check_region_flavor_class.rst

choose_flavor_class                    = /cloud_config/compute/cloud_servers_product_concepts/flavor_class/choose_flavor_class.rst

cinder                                 = /cloud_interfaces/CLI/cinder.rst

cloud_config                           = /cloud_config/index.rst

cloud_config_compute                   = /cloud_config/compute/index.rst

cloud_config_network                   = /cloud_config/network/index.rst

cloud_config_storage                   = /cloud_config/storage/index.rst

cloud_block_storage_product_concepts   = /cloud_config/storage/cloud_block_storage_product_concepts/index.rst

cloud_guide_intro                      = /cloud_guide_intro/index.rst

cloud_images_product_actions           = /cloud_config/compute/cloud_images_product_actions/index.rst
 
cloud_images_product_concepts          = /cloud_config/compute/cloud_images_product_concepts/index.rst

cloud_images_sharing                   = /cloud_config/compute/cloud_images_product_concepts/sharing_images/index.rst

cloud_images_sharing_planning          = /cloud_config/compute/cloud_images_product_concepts/sharing_images/planning.rst

cloud_images_sharing_models            = /cloud_config/compute/cloud_images_product_concepts/sharing_images/models.rst

cloud-init_boot                        = /cloud_config/compute/cloud_servers_product_concepts/boot/cloud-init_boot.rst

cloud_interfaces                       = /cloud_interfaces/index.rst

cloud_interfaces_API                   = /cloud_interfaces/API/index.rst

cloud_interfaces_CLI                   = /cloud_interfaces/CLI/index.rst

cloud_interfaces_GUI                   = /cloud_interfaces/GUI/index.rst

cloud_intro                            = /cloud_intro/index.rst

cloud_networks_DNS                     = /cloud_config/network/cloud_networks_product_concepts/DNS.rst

cloud_networks_product_actions         = /cloud_config/network/cloud_networks_product_actions/index.rst

cloud_networks_product_concepts        = /cloud_config/network/cloud_networks_product_concepts/index.rst

cloud_ops                              = /cloud_ops/index.rst

cloud_preprod                          = /cloud_preprod/index.rst

cloud_servers_flavor_class             = /cloud_config/compute/cloud_servers_product_concepts/flavor_class/index.rst

cloud_servers_metadata                 = /cloud_config/compute/cloud_servers_product_concepts/metadata/index.rst

cloud_servers_product_actions          = /cloud_config/compute/cloud_servers_product_actions/index.rst

cloud_servers_product_concepts         = /cloud_config/compute/cloud_servers_product_concepts/index.rst

cloud_tour                             = /cloud_intro/cloud_tour/index.rst

cloudblockstorage_API                  = /cloud_interfaces/API/cloudblockstorage_API.rst
cloudblockstorage_APIdemonstration     = /cloud_interfaces/API/cloudblockstorage_API.rst
cloudblockstorage_APIinvestigation     = /cloud_interfaces/API/cloudblockstorage_API.rst

cloudblockstorage_CLI                  = /cloud_interfaces/CLI/cloudblockstorage_CLI.rst

cloudblockstorage_GUI                  = /cloud_interfaces/GUI/cloudblockstorage_GUI.rst

cloudimages_API                        = /cloud_interfaces/API/cloudimages_API.rst
cloudimages_APIdemonstration           = /cloud_interfaces/API/cloudimages_API.rst
cloudimages_APIinvestigation           = /cloud_interfaces/API/cloudimages_API.rst

cloudimages_CLI                        = /cloud_interfaces/CLI/cloudimages_CLI.rst

cloudimages_GUI                        = /cloud_interfaces/GUI/cloudimages_GUI.rst

cloudnetworks_API                      = /cloud_interfaces/API/cloudnetworks_API.rst
cloudnetworks_APIdemonstration         = /cloud_interfaces/API/cloudnetworks_API.rst
cloudnetworks_APIinvestigation         = /cloud_interfaces/API/cloudnetworks_API.rst

cloudnetworks_CLI                      = /cloud_interfaces/CLI/cloudnetworks_CLI.rst

cloudnetworks_GUI                      = /cloud_interfaces/GUI/cloudnetworks_GUI.rst

cloudservers_API                       = /cloud_interfaces/API/cloudservers_API.rst
cloudservers_APIdemonstration          = /cloud_interfaces/API/cloudservers_API.rst
cloudservers_APIinvestigation          = /cloud_interfaces/API/cloudservers_API.rst

cloudservers_CLI                       = /cloud_interfaces/CLI/cloudservers_CLI.rst

cloudservers_GUI                       = /cloud_interfaces/GUI/cloudservers_GUI.rst

contactus                              = /cloud_guide_intro/contactus.rst

context                                = /cloud_intro/context.rst

core_infrastructure                    = /cloud_intro/core_infrastructure.rst

create_server                          = /cloud_config/compute/cloud_servers_product_concepts/create_server.rst

curl                                   = /cloud_interfaces/CLI/curl.rst

custom_images                          = /cloud_config/compute/cloud_images_product_concepts/custom_images.rst

customer_stories                       = /cloud_intro/customer_stories.rst

data_immutability                      = /cloud_config/compute/cloud_images_product_concepts/data_immutability.rst

default_base_images                    = /cloud_config/compute/cloud_images_product_concepts/base_images/default_base_images.rst

devopstools                            = /cloud_interfaces/API/devopstools.rst

disk_storage                           = /cloud_config/storage/cloud_block_storage_product_concepts/disk_storage.rst

diskconfig                             = /cloud_config/compute/cloud_servers_product_concepts/diskconfig.rst

document_history                       = /cloud_guide_intro/document_history.rst

drive_boot                             = /cloud_config/compute/cloud_servers_product_concepts/boot/drive_boot.rst

glance                                 = /cloud_interfaces/CLI/glance.rst

host_issues                            = /cloud_config/compute/cloud_servers_product_concepts/host_issues.rst

image_properties                       = /cloud_config/compute/cloud_images_product_concepts/image_properties.rst

import_export_images                   = /cloud_config/compute/cloud_images_product_concepts/import_export_images.rst

index                                  = index.rst (**home page for the site**)

lifecycle_base_images                  = /cloud_config/compute/cloud_images_product_concepts/base_images/lifecycle_base_images.rst

limits                                 = /cloud_ops/limits.rst

local_storage                          = /cloud_config/storage/cloud_block_storage_product_concepts/local_storage.rst

monitoring                             = /cloud_preprod/monitoring.rst

moreinfo                               = /cloud_guide_intro/moreinfo.rst

moreinfo_API                           = /cloud_interfaces/API/moreinfo_API.rst

moreinfo_CLI                           = /cloud_interfaces/CLI/moreinfo_CLI.rst

moreinfo_GUI                           = /cloud_interfaces/GUI/moreinfo_GUI.rst

network_cloud_servers                  = /cloud_config/network/cloud_networks_product_concepts/network_cloud_servers.rst
network_cloud_servers-working          = /cloud_config/network/cloud_networks_product_concepts/network_cloud_servers.rst

network_onmetal_servers                = /cloud_config/network/cloud_networks_product_concepts/network_onmetal_servers.rst

network_rackconnect                    = /cloud_config/network/cloud_networks_product_concepts/network_rackconnect.rst

neutron                                = /cloud_interfaces/CLI/neutron.rst

nova                                   = /cloud_interfaces/CLI/nova.rst

nova-agent                             = /cloud_config/compute/cloud_servers_product_concepts/nova-agent.rst

on-demand_images                       = /cloud_config/compute/cloud_images_product_concepts/on-demand_images.rst

patching_base_images                   = /cloud_config/compute/cloud_images_product_concepts/base_images/patching_base_images.rst

personality_boot                       = /cloud_config/compute/cloud_servers_product_concepts/boot/personality_boot.rst

publicnet                              = /cloud_config/network/cloud_networks_product_concepts/publicnet.rst

scaling                                = /cloud_preprod/scaling.rst

SDK                                    = /cloud_interfaces/API/SDK.rst

security                               = /cloud_preprod/security.rst

scheduled_images                       = /cloud_config/compute/cloud_images_product_concepts/scheduled_images.rst

server_events                          = /cloud_config/compute/cloud_servers_product_concepts/server_events.rst

server_region                          = /cloud_config/compute/cloud_servers_product_concepts/server_region.rst

servicenet                             = /cloud_config/network/cloud_networks_product_concepts/servicenet.rst

set_metadata                           = /cloud_config/compute/cloud_servers_product_concepts/metadata/set_metadata.rst

setup_API                              = /cloud_interfaces/API/setup_API.rst

setup_CLI                              = /cloud_interfaces/CLI/setup_CLI.rst

setup_GUI                              = /cloud_interfaces/GUI/setup_GUI.rst

show_metadata                          = /cloud_config/compute/cloud_servers_product_concepts/metadata/show_metadata.rst

software_RAID                          = /cloud_config/storage/cloud_block_storage_product_concepts/software_RAID.rst

somethingnew                           = /cloud_ops/somethingnew.rst

SSH                                    = /cloud_config/compute/cloud_servers_product_concepts/SSH.rst

stack                                  = /cloud_preprod/stack.rst 

supernova                              = /cloud_interfaces/CLI/supernova.rst

support                                = /cloud_ops/support.rst

time                                   = /cloud_config/compute/cloud_servers_product_concepts/time.rst

tour_application_services              = /cloud_intro/cloud_tour/application_services.rst

tour_compute_services                  = /cloud_intro/cloud_tour/compute_services.rst

tour_data_services                     = /cloud_intro/cloud_tour/data_services.rst

tour_network_services                  = /cloud_intro/cloud_tour/network_services.rst

tour_storage_services                  = /cloud_intro/cloud_tour/storage_services.rst

tour_support_services                  = /cloud_intro/cloud_tour/support_services.rst

troubleshoot                           = /cloud_ops/troubleshoot.rst

virtualization_modes                   = /cloud_config/compute/cloud_images_product_concepts/virtualization_modes.rst

