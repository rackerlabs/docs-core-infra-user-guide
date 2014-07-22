Personality
===========

Allows user specified files to be injected into a server's file system at boot. Personality only supports text files that are Base64 encoded and does not support binary or zip files. A file path on the remote server is required as well as a path to the local file. The maximum file path is 255 bytes. Up to 5 different file/path content pairs may be included, that max size for each pair can not exceed 1000 bytes. This limit is for the number of decoded bytes and not encoded.

If a larger file size limit is required it is recommended to use config drive instead.

If the file already exists on the remote server it will be renamed with a *.bak* extension and a timestamp appended *.bak.1246036261.5785*. The file will be owned by the root user and a member or the root group.