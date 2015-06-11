.. _show_metadata:

^^^^^^^^^^^^^^^^
Showing metadata
^^^^^^^^^^^^^^^^
To view the metadata on a Cloud Server, use the ``nova show`` command with
the desired Cloud Server ID::

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
with this Cloud Server. 
:ref:`set_metadata` shows how you can create or delete metadata. 

Some metadata are set by Rackspace and not available to be changed by
the user; generally these fields are used by automation and
orchestration systems needed to properly build and maintainer your Cloud
Server.

The metadata that are attached to your server are also stored if you
create a snapshot or image from the server, and restored when a server is
built from that image. The key names are prefixed with ``instance\_``.
