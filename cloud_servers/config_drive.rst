Config Drive
============
Config drive is a read only ISO9660 formatted, un-partitioned, 64MB block device that is attached to a server during build. By default this drive contains server specific metadata such as networking at launch. User specified files can be added to this drive for the purpose of injecting data into the server.

Config drive must be mounted in order for the contents to be accessed, if the operating system supports accessing disk by label config drive will be labeled as **config-2**.

Config drive is used primarily as a data source for cloud-init, if cloud-init or cloudbase-init is present the drive will automatically be mounted. 