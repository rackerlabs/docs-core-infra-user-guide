.. _set-metadata:

+++++++++++++++++++++++++++++
Setting and updating metadata
+++++++++++++++++++++++++++++
To set or change metadata on a cloud server, use the ``nova meta`` command
with the action ``set``, and provide the cloud server ID and key/value
pair that you want to set or update:

.. code-block:: bash

   $ nova meta 191ecc6d-a4aa-4cdd-979f-536c55857c90 set useful-key=useful-value

Your custom metadata appears when you issue a ``show`` command on your server.

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

In general, you can use any metadata key that you need, as long as it doesn't
conflict with existing metadata placed on the server by Rackspace,
and doesn't exceed 255 characters.

To delete a metadata key from a server, use the ``nova meta``
command with the action ``delete``, and provide the server ID and
the key that you want to remove:

.. code-block:: bash

   $ nova meta 191ecc6d-a4aa-4cdd-979f-536c55857c90 delete useful-key

Now when you look at your server, your metadata item is gone:

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
   | metadata | {}                                                                           |
   | name     | My Server                                                                    |
   | status   | ACTIVE                                                                       |
   +----------+------------------------------------------------------------------------------+

After a metadata field is deleted, it cannot be recovered.

.. include:: /_common/seealso-concepts-cloud-servers.txt
