.. _network-ssh:

----------------------------
Validating SSH configuration
----------------------------
Depending on your circumstances, it may be appropriate for you to change the
assignment of port 22 in your configuration. By default, port 22 is assigned to
:how-to:`Secure Shell (SSH) <connecting-to-a-server-using-ssh-on-linux-or-mac-os>`.
Changing this assignment can make it harder for attackers to
guess the location your SSH port, but that change can also make it impossible for some
cloud services to coordinate their activities.

.. WARNING::
   **Do not change the default assignment of your SSH port
   if any of the following are true of your account:**

   - Uses Managed Operations service level
   - Uses RackConnect
   - Uses Cloud Monitoring
   - Uses Cloud Backup

Before you make any change to the SSH port,
make sure you can answer the following questions:

- *Does your account use the Managed Operations service level?*

  To learn which service level is associated with your account,
  login to the
  :mycloud:`Cloud Control Panel <>`.
  At the upper right, under your account name, look for a red **+** followed by
  the shortened name of a Rackspace service level. For example,
  **Managed Infrastructure** is indicated by "+Infrastructure".

  You can compare the Managed Infrastructure and Managed Operations
  service levels at
  :rax-cloud:`Compare service levels <compare-service-levels>`.

- *Does your account use RackConnect?*

  :rax-cloud:`RackConnect <hybrid/rackconnect>` enables cloud servers and
  dedicated servers to share data.
  On the :mycloud:`Cloud Control Panel <>`, nothing indicates which cloud
  servers use RackConnect to communicate with dedicated servers.

  RackConnect configurations are managed from the
  `MyRack control panel <https://my.rackspace.com/>`_,
  where dedicated devices are managed.
  When you login to the
  `MyRack control panel <https://my.rackspace.com/>`_
  and display **Server Details** for a cloud server, the details include
  a **RackConnect Status** field.
  If **RackConnect Status** is **Deployed** for at least one server,
  then RackConnect is in use at your account.
  You can read more about this at
  :how-to:`Accessing RackConnect Cloud Servers <accessing-rackconnect-cloud-servers>`.

- *Does your account use Cloud Monitoring?*

  :rax-cloud:`Cloud Monitoring <monitoring>`
  is available to all Rackspace cloud customers.
  Even if you have not chosen to
  use Cloud Monitoring to observe activity on servers that interest you,
  someone at your account may be using Cloud Monitoring to enable
  :rax-cloud:`Auto Scale <auto-scale>`.

  To learn whether Auto Scale is in use at your account,
  login to the
  :mycloud:`Cloud Control Panel <>`.
  On the **Servers** menu,
  click **Auto Scale**.
  If Auto Scale is in use, at least one scaling group is listed under **Groups**.
  Otherwise, a message reports that no scaling groups have been created.

  .. figure:: /_images/autoscale-nogroups.png
     :scale: 80%
     :alt: If anyone at your account is using Auto Scale,
           a scaling group is listed.

     *If anyone at your account is using Auto Scale,
     a scaling group is listed.*

- *Does your account use Cloud Backup?*

  :rax-cloud:`Cloud Backup <backup>`
  is available to all Rackspace cloud customers.
  Even if you have not chosen to
  use Cloud Backup to maintain copies of key data on servers that interest you,
  someone at your account may be using Cloud Backup
  to protect data on other servers.

  To learn whether Cloud Backup is in use at your account,
  login to the
  :mycloud:`Cloud Control Panel <>`.
  On the **Backups** menu,
  click **Activity**.
  If Cloud Backup is in use, at least one backup schedule is listed.
  Otherwise, a message reports that no backup activity was found.

Whether you reassign port 22 or retain this default assignment,
your best security comes from an effective firewall configuration.
