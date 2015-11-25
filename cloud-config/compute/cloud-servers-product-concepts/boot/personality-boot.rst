.. _personality-boot:

++++++++++++++++++++++++++++++++++++++++++
Controlling boot behavior with personality
++++++++++++++++++++++++++++++++++++++++++
*Personality* enables user-specified files to be injected into a server's
file system at boot. Personality supports only text files that are
Base64-encoded and does not support binary or zip files.

A file path on the remote server is required as well as
a path to the local file. The maximum length of the file path is
255 bytes. Up to five different file/path content
pairs can be included.

If you specify a file for injection that already exists on the remote
server, the pre-existing file is renamed with a **.bak** extension
and a time stamp is appended, such as **.bak.1246036261.5785**.
The **.bak** file is owned by the root user and a member of the root group.

The maximum size for each pair cannot exceed 1,000 decoded (versus
encoded) bytes. If a larger file size limit is required, we recommend
using a config drive instead.

.. include:: /_common/seealso-concepts-cloud-servers.txt
