Cloud-init
==========
Cloud-init is a multi-distribution open source package developed by Canonical that handles the early initialization of a server running Linux. Cloud-init's behavior can be configured via customer supplied user-data. User-data is supplied via a config file written in cloud-config specific syntax that contains directives on how cloud-init should behave. 

More Information
http://cloudinit.readthedocs.org/en/latest/

In the Rackspace environment cloud-init handles some of the server setup actions traditionally preformed by the nova-agent. This varies from image to image but as of today cloud-init handles the disk expansion and partitioning for Linux PVHVM images. 