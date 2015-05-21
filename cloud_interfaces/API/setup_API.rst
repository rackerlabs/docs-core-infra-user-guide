.. _setup_API:

------------------------------
Preparing to use SDKs and APIs
------------------------------
If you have a Rackspace cloud account, you can use Rackspace APIs 
to interact with the cloud services you subscribe to. 

The basic process is the same for all Rackspace APIs:

1. Collect parts needed for the request:

  * Obtain your account credentials 
    (`API key <http://www.rackspace.com/knowledge_center/article/view-and-reset-your-api-key>`__
    and account number, also called tenant ID)
    from the 
    `Cloud Control Panel <https://mycloud.rackspace.com/>`__.
   
   
  * `Use your credentials to authenticate <http://docs.rackspace.com/auth/api/v2.0/auth-client-devguide/content/QuickStart-000.html>`__, 
    receiving a token and a service catalog as proof of success
    
    
  * In the 
    `service catalog <http://docs.rackspace.com/auth/api/v2.0/auth-client-devguide/content/Sample_Request_Response-d1e64.html>`__,
    find the endpoint for the API to which you want to send a request.
    
    
  * Look up the 
    `syntax of the API request <http://api.rackspace.com/>`__. 

 
2. Assemble the request from its parts.

 
  Plug in the values you collected for your credentials, 
  the API's endpoint, 
  and any details (such as the ID of a server) 
  specific to your configuration and your API request. 
 

3. Send a well-formed request to the service's API endpoint.

 
4. Process the service's response.
 

Beyond this general process, the details vary 
depending on which service you are working with. 
For product-specific introductions to 
the SDKs and APIs relevant to specific 
core infrastructure products, see

* :ref:`cloudservers_API`
* :ref:`cloudnetworks_API`
* :ref:`cloudimages_API`
* :ref:`cloudblockstorage_API`
