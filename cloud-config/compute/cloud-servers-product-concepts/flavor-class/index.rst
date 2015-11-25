.. _cloud-servers-flavor-class:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Understanding flavor classes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A flavor class is a grouping of flavors based on similar
characteristics. Flavor classes streamline the process
of choosing among
available resources and pricing models.

When you create a cloud server,
the server's configuration is based on your
answers to several questions:

* **Which server technology (virtual or OnMetal™)
  should the server use?**

  Compare :ref:`virtual-server-flavor-class` and
  :ref:`onmetal-server-flavor-class` to help you consider
  the differences.

* **In which region will the server be based?**

  Most flavor classes are available everywhere, but a few
  are only available in some regions.
  :ref:`check-region-flavor-class` shows how to tell
  which flavor classes are available in your server's region.

* **Of the flavor classes available to that server technology,
  which is best suited to the workload planned for
  the new server?**

* **Of the flavors available within that flavor class,
  which provides the right-sized and right-priced
  configuration?**

  Choose a flavor class based on your expectations
  of the server's primary workload.
  For example, you can choose a flavor class optimized for I/O if
  you expect the cloud server to support an I/O-intensive workload.
  Within the flavor class, you then choose a specific flavor based
  on the configuration options you prefer.
  You can learn more about this at
  :ref:`choose-flavor-class`.

.. include:: /_common/seealso-concepts-cloud-servers.txt

.. toctree:: :hidden:
   :maxdepth: 2

   virtual-server-flavor-class
   onmetal-server-flavor-class
   check-region-flavor-class
   choose-flavor-class
