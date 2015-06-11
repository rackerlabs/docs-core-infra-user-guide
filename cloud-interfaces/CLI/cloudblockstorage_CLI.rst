.. _cloudblockstorage_CLI:

------------------------------------
Cloud Block Storage and CLIs: cinder
------------------------------------
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

You can also use the 
:ref:`cinder`, 
focused on Cloud Block Storage. 

In working with Cloud Block Storage, 
you may find that you need to use nova for some functions 
and cinder for others. You should install them both. 
You can see an example of using nova and cinder together at 
`Configuring OpenStack Block Storage <http://www.rackspace.com/knowledge_center/article/configuring-openstack-block-storage>`__ 
where, in the "Create a Volume" section, 
``nova volume-attach`` associates a volume with a server 
and ``cinder list`` confirms that association. 

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
`API cross-reference <http://api.rackspace.com/api-ref-blockstorage.html>`__ 
lists those requests for Cloud Block Storage. 

The Getting Started Guide for the Cloud Block Storage API 
includes many examples of using cURL, especially at 
`Using the API directly by using cURL <http://docs.rackspace.com/cbs/api/v1.0/cbs-getting-started/content/Using_the_API_directly_d1e060.html>`__.
 
If you have both the cinder client and cURL 
installed on your local machine, 
you can choose whether to issue commands through your 
local copy of the cinder client or, by using a general-purpose client 
such as cURL, by sending a request to the instance of 
python-cinderclient active at the API endpoint for 
Cloud Block Storage. 
You can see both methods demonstrated in the Cloud Block Storage 
API documentation, under 
`Cloud Block Storage quotas <http://docs.rackspace.com/cbs/api/v1.0/cbs-devguide/content/serviceQuotas-d1e01.html>`_.

* cinder users send ``cinder quota-usage yourAccountID``
* cURL users send ``curl -i -X GET https://dfw.blockstorage.api.rackspacecloud.com/v1/yourAccountID/os-quota-sets/yourAccountID?usage=True \
  -H "X-Auth-Project-Id: yourAccountID" \
  -H "User-Agent: python-cinderclient" \
  -H "Accept: application/json" \
  -H "X-Auth-Token: yourAuthToken"``

Contents:

.. toctree::
   :maxdepth: 2  

   cinder