.. _show-metadata:

++++++++++++++++
Showing metadata
++++++++++++++++
To view the metadata on a cloud server, use the ``nova show`` command with
the appropriate server ID, as shown in the following example:

.. code-block:: bash

   $ nova show 191ecc6d-a4aa-4cdd-979f-536c55857c90

   +----------+------------------------------------------------------------------------------+
   | Property | Value                                                                        |
   +----------+------------------------------------------------------------------------------+
   | created  | 2014-11-18T22:02:06Z                                                         |
   | flavor   | 1 GB General Purpose v1 (general1-1)                                         |
   | hostId   | a9ebad0b0650501b632c44790b5444eeeff7e824101d13c087815b37                     |
   | id       | 191ecc6d-a4aa-4cdd-979f-536c55857c90                                         |
   | image    | Ubuntu 14.10 (Utopic Unicorn) (PVHVM) (0766e5df-d60a-4100-ae8c-07f27ec0148f) |
   | metadata | {"useful-key": "useful-value"}                                               |
   | name     | My Server                                                                    |
   | status   | ACTIVE                                                                       |
   +----------+------------------------------------------------------------------------------+

The ``metadata`` property shows user-defined metadata associated
with this server.
:ref:`set-metadata` shows how you can create or delete metadata.

Some metadata are set by Rackspace and not available to be changed by
the user. Generally these metadata are used by automation and
orchestration systems needed to correctly build and maintain your server.

The metadata that are attached to your server are also stored if you
create a snapshot or image from the server, and are restored when a server is
built from that image. The key names are prefixed with ``instance_``.

.. include:: /_common/seealso-concepts-cloud-servers.txt
