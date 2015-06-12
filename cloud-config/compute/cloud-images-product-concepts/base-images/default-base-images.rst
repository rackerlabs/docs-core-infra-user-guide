.. default_base_images:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Default base image configurations
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
How we manage the default configuration for base images is different for
different kinds of accounts.

* For **Managed Infrastructure** accounts, we keep the base configuration
  as close as we can to distribution defaults. Some changes are
  necessary in order for us to properly support the operating system in
  our environment. We try to keep these changes to a minimum so users
  know exactly what behavior to expect.

* For **Managed Operations** accounts, post-build automation runs to
  configure the operating system according to Rackspace best practices.

* For **RackConnect** accounts, default networking configurations are
  changed as needed.
