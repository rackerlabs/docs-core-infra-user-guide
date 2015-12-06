.. _network-ssh:

----------------------------
Validating SSH configuration
----------------------------
Depending on your circumstances, it may be appropriate for you to change the
assignment of port 22 in your configuration. By default, port 22 is assigned to
Secure Shell (SSH). Changing this assignment can make it harder for attackers to
locate your SSH port, but that change can also make it impossible for some
cloud services to coordinate their activities.

If any of the following are true of your configuration,
do not change the default assignment of your SSH port:

- Uses Cloud Servers with a Managed Operations service level.

  *To confirm this, login to the Cloud Control Panel.
  At the upper right, under your account name, look for a red **+* followed by
  the shortened name of a Rackspace service level. For example,
  **Managed Infrastructure** is indicated by "+Infrastructure".

  You can compare the Managed Infrastructure and Managed Operations
  service levels at
  :rax-cloud:`Compare service levels <compare-service-levels>`.

- Uses RackConnect.

  *To confirm this, X*

- Uses Cloud Monitoring.

  *To confirm this, X*

- Uses Cloud Backup.

  *To confirm this, X*

Whether you reassign port 22 or retain this default assignment,
your best security comes from an effective firewall configuration.
