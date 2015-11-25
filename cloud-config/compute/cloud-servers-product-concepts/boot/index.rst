.. _boot:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Controlling cloud server initiation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
You can configure your cloud server so that
when it is started or restarted, it
initiates operation in any of several ways:

* Boot from
  :ref:`drive <drive-boot>`
  if you want to
  boot from the
  read-only drive configured with
  your server.

* Boot from
  :ref:`personality <personality-boot>`
  if you want to
  inject your own files
  into the boot process.


* Boot from
  :ref:`cloud-init <cloud-init-boot>`
  if you want to
  customize your boot with a
  cloud-init config file.

  .. include:: /_common/seealso-concepts-cloud-servers.txt


.. toctree:: :hidden:
   :maxdepth: 2

   drive-boot
   personality-boot
   cloud-init-boot
