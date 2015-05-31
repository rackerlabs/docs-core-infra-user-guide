.. personality_boot:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Controlling boot behavior with personality
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Personality allows user-specified files to be injected into a server's
file system at boot. Personality only supports text files that are
Base64 encoded and does not support binary or zip files. A file path on
the remote server is required as well as a path to the local file. The
maximum file path is 255 bytes. Up to 5 different file/path content
pairs may be included.

If you specify a file for injection that already exists on the remote
server, the pre-existing file will be renamed with a ``.bak`` extension
and a timestamp appended, such as ``.bak.1246036261.5785``. 
The ``.bak``
file will be owned by the root user and a member of the root group.

The maximum size for each pair cannot exceed 1000 decoded (versus
encoded) bytes. If a larger file size limit is required, we suggest
using a config drive instead.
