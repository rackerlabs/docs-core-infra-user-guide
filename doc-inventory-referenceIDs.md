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

assumptions                            = /cloud-guide-intro/assumptions.rst

backup-methods                         = /cloud-config/storage/cloud-block-storage-product-concepts/backup-methods.rst

backups                                = /cloud-preprod/backups.rst

base-images                            = /cloud-config/compute/cloud-images-product-concepts/base-images/index.rst

bestpractice                           = /cloud-ops/bestpractice.rst

block-storage                          = /cloud-config/storage/cloud-block-storage-product-actions/block-storage.rst

boot                                   = /cloud-config/compute/cloud-servers-product-concepts/boot/index.rst

change-server                          = /cloud-config/compute/cloud-servers-product-concepts/change-server.rst

check-region-flavor-class              = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/check-region-flavor-class.rst

choose-flavor-class                    = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/choose-flavor-class.rst

cinder                                 = /cloud-interfaces/cli/cinder.rst

cloud-config                           = /cloud-config/index.rst

cloud-config-compute                   = /cloud-config/compute/index.rst

cloud-config-network                   = /cloud-config/network/index.rst

cloud-config-storage                   = /cloud-config/storage/index.rst

cloud-block-storage-product-actions    = /cloud-config/storage/cloud-block-storage-product-actions/index.rst

cloud-block-storage-product-concepts   = /cloud-config/storage/cloud-block-storage-product-concepts/index.rst

cloud-guide-intro                      = /cloud-guide-intro/index.rst

cloud-images-product-actions           = /cloud-config/compute/cloud-images-product-actions/index.rst

cloud-images-product-concepts          = /cloud-config/compute/cloud-images-product-concepts/index.rst

cloud-images-sharing                   = /cloud-config/compute/cloud-images-product-concepts/sharing-images/index.rst

cloud-images-sharing-managing          = /cloud-config/compute/cloud-images-product-concepts/sharing-images/managing.rst

cloud-images-sharing-planning          = /cloud-config/compute/cloud-images-product-concepts/sharing-images/planning.rst

cloud-images-sharing-preparing         = /cloud-config/compute/cloud-images-product-concepts/sharing-images/preparing.rst

cloud-images-sharing-roles             = /cloud-config/compute/cloud-images-product-concepts/sharing-images/roles.rst

cloud-images-sharing-support           = /cloud-config/compute/cloud-images-product-concepts/sharing-images/support.rst

cloud-init-boot                        = /cloud-config/compute/cloud-servers-product-concepts/boot/cloud-init-boot.rst

cloud-interfaces                       = /cloud-interfaces/index.rst

cloud-interfaces-api                   = /cloud-interfaces/api/index.rst

cloud-interfaces-cli                   = /cloud-interfaces/cli/index.rst

cloud-interfaces-gui                   = /cloud-interfaces/gui/index.rst

cloud-intro                            = /cloud-intro/index.rst

cloud-networks-product-actions         = /cloud-config/network/cloud-networks-product-actions/index.rst

cloud-networks-product-concepts        = /cloud-config/network/cloud-networks-product-concepts/index.rst

cloudnetworks-benefits                 = /cloud-config/network/cloud-networks-product-concepts/cloudnetworks-benefits.rst

cloudnetworks-usecases                 = /cloud-config/network/cloud-networks-product-concepts/cloudnetworks-usecases.rst

cloud-ops                              = /cloud-ops/index.rst

cloud-preprod                          = /cloud-preprod/index.rst

cloud-servers-flavor-class             = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/index.rst

cloud-servers-metadata                 = /cloud-config/compute/cloud-servers-product-concepts/metadata/index.rst

cloud-servers-product-actions          = /cloud-config/compute/cloud-servers-product-actions/index.rst

cloud-servers-product-concepts         = /cloud-config/compute/cloud-servers-product-concepts/index.rst

cloud-tour                             = /cloud-intro/cloud-tour/index.rst

cloudblockstorage-api                  = /cloud-interfaces/api/cloudblockstorage-api.rst
cloudblockstorage-apidemonstration     = /cloud-interfaces/api/cloudblockstorage-api.rst
cloudblockstorage-apiinvestigation     = /cloud-interfaces/api/cloudblockstorage-api.rst

cloudblockstorage-cli                  = /cloud-interfaces/cli/cloudblockstorage-cli.rst

cloudblockstorage-gui                  = /cloud-interfaces/gui/cloudblockstorage-gui.rst

cloudimages-api                        = /cloud-interfaces/api/cloudimages-api.rst
cloudimages-apidemonstration           = /cloud-interfaces/api/cloudimages-api.rst
cloudimages-apiinvestigation           = /cloud-interfaces/api/cloudimages-api.rst

cloudimages-cli                        = /cloud-interfaces/cli/cloudimages-cli.rst

cloudimages-gui                        = /cloud-interfaces/gui/cloudimages-gui.rst

cloudnetworks-api                      = /cloud-interfaces/api/cloudnetworks-api.rst
cloudnetworks-apidemonstration         = /cloud-interfaces/api/cloudnetworks-api.rst
cloudnetworks-apiinvestigation         = /cloud-interfaces/api/cloudnetworks-api.rst

cloudnetworks-cli                      = /cloud-interfaces/cli/cloudnetworks-cli.rst

cloudnetworks-gui                      = /cloud-interfaces/gui/cloudnetworks-gui.rst

cloudservers-api                       = /cloud-interfaces/api/cloudservers-api.rst
cloudservers-apidemonstration          = /cloud-interfaces/api/cloudservers-api.rst
cloudservers-apiinvestigation          = /cloud-interfaces/api/cloudservers-api.rst

cloudservers-cli                       = /cloud-interfaces/cli/cloudservers-cli.rst

cloudservers-gui                       = /cloud-interfaces/gui/cloudservers-gui.rst

contactus                              = /cloud-guide-intro/contactus.rst

context                                = /cloud-intro/context.rst

core-infrastructure                    = /cloud-intro/core-infrastructure.rst

create-server                          = /cloud-config/compute/cloud-servers-product-concepts/create-server.rst

curl                                   = /cloud-interfaces/cli/curl.rst

custom-images                          = /cloud-config/compute/cloud-images-product-concepts/custom-images.rst

customer-stories                       = /cloud-intro/customer-stories.rst

data-immutability                      = /cloud-config/compute/cloud-images-product-concepts/data-immutability.rst

default-base-images                    = /cloud-config/compute/cloud-images-product-concepts/base-images/default-base-images.rst

devopstools                            = /cloud-interfaces/api/devopstools.rst

direct-api-access                      = /cloud-interfaces/api/direct-api-access.rst

disk-storage                           = /cloud-config/storage/cloud-block-storage-product-concepts/disk-storage.rst

diskconfig                             = /cloud-config/compute/cloud-servers-product-concepts/diskconfig.rst

dns                                    = /cloud-config/network/cloud-networks-product-concepts/dns.rst

document-history                       = /cloud-guide-intro/document-history.rst

drive-boot                             = /cloud-config/compute/cloud-servers-product-concepts/boot/drive-boot.rst

glance                                 = /cloud-interfaces/cli/glance.rst

host-issues                            = /cloud-config/compute/cloud-servers-product-concepts/host-issues.rst

image-properties                       = /cloud-config/compute/cloud-images-product-concepts/image-properties.rst

import-export-images                   = /cloud-config/compute/cloud-images-product-concepts/import-export-images.rst

index                                  = index.rst (**home page for the site**)

lifecycle-base-images                  = /cloud-config/compute/cloud-images-product-concepts/base-images/lifecycle-base-images.rst

limits                                 = /cloud-ops/limits.rst

local-storage                          = /cloud-config/storage/cloud-block-storage-product-concepts/local-storage.rst

monitoring                             = /cloud-preprod/monitoring.rst

moreinfo                               = /cloud-guide-intro/moreinfo.rst

moreinfo-api                           = /cloud-interfaces/api/moreinfo-api.rst

moreinfo-cli                           = /cloud-interfaces/cli/moreinfo-cli.rst

moreinfo-gui                           = /cloud-interfaces/gui/moreinfo-gui.rst

network-cloud-servers                  = /cloud-config/network/cloud-networks-product-concepts/network-cloud-servers.rst

network-cloud-servers-working          = /cloud-config/network/cloud-networks-product-concepts/network-cloud-servers.rst

network-gateway-instances              = /cloud-config/network/cloud-networks-product-concepts/network-gateway-instances.rst

network-onmetal-servers                = /cloud-config/network/cloud-networks-product-concepts/network-onmetal-servers.rst

network-rackconnect                    = /cloud-config/network/cloud-networks-product-concepts/network-rackconnect.rst

network-ssh                            = /cloud-preprod/network-ssh.rst

neutron                                = /cloud-interfaces/cli/neutron.rst

nova                                   = /cloud-interfaces/cli/nova.rst

nova-agent                             = /cloud-config/compute/cloud-servers-product-concepts/nova-agent.rst

on-demand-images                       = /cloud-config/compute/cloud-images-product-concepts/on-demand-images.rst

onmetal-server-flavor-class            = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/onmetal-server-flavor-class.rst

patching-base-images                   = /cloud-config/compute/cloud-images-product-concepts/base-images/patching-base-images.rst

personality-boot                       = /cloud-config/compute/cloud-servers-product-concepts/boot/personality-boot.rst

publicnet                              = /cloud-config/network/cloud-networks-product-concepts/publicnet.rst

scaling                                = /cloud-preprod/scaling.rst

sdk                                    = /cloud-interfaces/api/sdk.rst

security                               = /cloud-preprod/security.rst

security-groups                        = /cloud-config/network/cloud-networks-product-concepts/security-groups.rst

scheduled-images                       = /cloud-config/compute/cloud-images-product-concepts/scheduled-images.rst

server-events                          = /cloud-config/compute/cloud-servers-product-concepts/server-events.rst

server-region                          = /cloud-config/compute/cloud-servers-product-concepts/server-region.rst

servicenet                             = /cloud-config/network/cloud-networks-product-concepts/servicenet.rst

servicenet-publicnet-requirement       = /cloud-config/network/cloud-networks-product-concepts/servicenet-publicnet-requirement.rst

set-metadata                           = /cloud-config/compute/cloud-servers-product-concepts/metadata/set-metadata.rst

setup-api                              = /cloud-interfaces/api/setup-api.rst

setup-cli                              = /cloud-interfaces/cli/setup-cli.rst

setup-gui                              = /cloud-interfaces/gui/setup-gui.rst

show-metadata                          = /cloud-config/compute/cloud-servers-product-concepts/metadata/show-metadata.rst

software-raid                          = /cloud-config/storage/cloud-block-storage-product-concepts/software-raid.rst

somethingnew                           = /cloud-ops/somethingnew.rst

ssh                                    = /cloud-config/compute/cloud-servers-product-concepts/ssh.rst

stack                                  = /cloud-preprod/stack.rst

supernova                              = /cloud-interfaces/cli/supernova.rst

support                                = /cloud-ops/support.rst

time                                   = /cloud-config/compute/cloud-servers-product-concepts/time.rst

tour-application-services              = /cloud-intro/cloud-tour/application-services.rst

tour-compute-services                  = /cloud-intro/cloud-tour/compute-services.rst

tour-data-services                     = /cloud-intro/cloud-tour/data-services.rst

tour-network-services                  = /cloud-intro/cloud-tour/network-services.rst

tour-storage-services                  = /cloud-intro/cloud-tour/storage-services.rst

tour-support-services                  = /cloud-intro/cloud-tour/support-services.rst

troubleshoot                           = /cloud-ops/troubleshoot.rst
troubleshoot-connectivity              = /cloud-ops/troubleshoot.rst
troubleshoot-build                     = /cloud-ops/troubleshoot.rst

virtual-server-flavor-class            = /cloud-config/compute/cloud-servers-product-concepts/flavor-class/virtual-server-flavor-class.rst
