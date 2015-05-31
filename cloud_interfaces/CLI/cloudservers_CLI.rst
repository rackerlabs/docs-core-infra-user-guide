.. _cloudservers_CLI:

------------------------------------------
Cloud Servers and CLIs: nova and supernova
------------------------------------------
To interact with Cloud Servers at the command line, 
you can use tools created specifically for the purpose 
of interacting with OpenStack-based clouds 
(nova, supernova) 
or general-purpose tools (cURL). 

Before you can use one of these tools, 
you must install a local (client) copy. 
The installation procedure varies for each tool 
and is documented with the tool. 

The commands you can send are the 
the same, 
wrapped in the syntax of the client, 
as the requests you can send 
to the API endpoint. 
The 
`API cross-reference <http://api.rackspace.com/api-ref.html#compute-core-v2>`__ 
lists those requests for Cloud Servers. 

Contents:

.. toctree::
   :maxdepth: 2  

   nova
   supernova
   curl