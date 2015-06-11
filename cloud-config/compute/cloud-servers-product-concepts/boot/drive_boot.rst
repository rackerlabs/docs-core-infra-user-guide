.. drive_boot:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Controlling boot behavior with a config drive
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
A config drive is a read-only, un-partitioned, 64 MB block device that
is attached to a server during build; the device is formatted to comply
with ISO 9960. By default this drive contains server-specific metadata
such as networking at launch. User-specified files can be added to this
drive for the purpose of injecting data into the server.

The config drive's contents are accessible only when the drive is mounted. 
If the operating system supports accessing disk by label, the
config drive is labeled ``config-2``.

The config drive is used primarily as a data source for cloud-init. If
cloud-init or cloudbase-init is present, the config drive is
automatically mounted.
