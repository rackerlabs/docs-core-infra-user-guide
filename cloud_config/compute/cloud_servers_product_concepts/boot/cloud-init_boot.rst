.. cloud-init_boot:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Controlling boot behavior with cloud-init
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Cloud-init is a multi-distribution open source package developed by
Canonical that handles the early initialization of a server running
Linux. Cloud-init's behavior can be configured via customer-supplied
user data. User data is supplied via a config file written in
cloud-config specific syntax that contains directives on how cloud-init
should behave.

More information about cloud-init is available in 
`cloud-init's documentation <http://cloudinit.readthedocs.org/en/latest/>`__.

In the Rackspace cloud, cloud-init is responsible for handling
some of the server setup actions traditionally preformed by the
nova-agent. This varies from image to image, but currently cloud-init
handles the disk expansion and partitioning for Linux PVHVM images.
