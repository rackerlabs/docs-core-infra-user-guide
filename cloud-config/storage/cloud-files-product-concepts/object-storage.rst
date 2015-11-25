.. _object-storage:

~~~~~~~~~~~~~~
Object storage
~~~~~~~~~~~~~~
At its core, Cloud Files is an object storage solution and is not
designed for high IOPS (Input/output Operations Per Second). Instead,
Cloud Files is designed for consistent reliability of data. The
primary function of Cloud Files is to ensure that your data is
available when you ask for it. This works best with relatively static files,
as opposed to files that are frequently updated.

An object is the basic storage entity and its metadata that represent
the files that you store in Cloud Files. When you upload data to
Cloud Files, the data is stored as-is (no compression or encryption) and
consists of a location (container), its name, and optional metadata
consisting of key/value pairs.

Objects are grouped into containers, and you can have any number of
objects within a container.

.. include:: /_common/seealso-concepts-cloud-files.txt
