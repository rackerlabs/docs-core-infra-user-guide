.. _default-base-images:

+++++++++++++++++++++++++++++++++
Default base image configurations
+++++++++++++++++++++++++++++++++
Default configurations for base images are managed differently for
different kinds of accounts.

* For **Managed Infrastructure** accounts, the base configuration is kept
  as close as possible to distribution defaults. Some changes are
  necessary to properly support the operating system in
  our environment, but these changes are kept to a minimum so users
  know exactly what behavior to expect.

* For **Managed Operations** accounts, post-build automation runs to
  configure the operating system according to Rackspace best practices.

* For **RackConnect** accounts, default networking configurations are
  changed as needed.

.. include:: /_common/seealso-concepts-cloud-images.txt
