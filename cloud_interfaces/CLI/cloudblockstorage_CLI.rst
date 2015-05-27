.. _cloudblockstorage_CLI:

---------------------------------------------
Cloud Block Storage and CLIs: nova and cinder
---------------------------------------------
To interact with Cloud Block Storage at the command line, 
you can use tools created specifically for the purpose 
of interacting with OpenStack-based clouds 
(nova, cinder) 
or general-purpose tools (cURL). 

Because Cloud Servers and Cloud Block Storage work so 
closely together, 
the command-line tools that work well with Cloud Servers 
also work well with Cloud Block Storage. 

You can read about these as a group at 
:ref:`cloudservers_CLI` 
or you can go directly to the tool that interests you:

* :ref:`nova`
* :ref:`supernova`
* :ref:`curl`

You can also use the cinder CLI, 
focused on Cloud Block Storage. 

Before you can use one of these tools, 
you must install a local (client) copy. 
The installation procedure varies for each tool 
and is documented with the tool. 

The commands you can send are the 
the same, 
wrapped in the syntax of the client, 
as the requests you can send 
to the API endpoint. 
http://api.rackspace.com/api-ref-blockstorage.html 
lists those requests for Cloud Networks. 

Contents:

.. toctree::
   :maxdepth: 2  

   cinder