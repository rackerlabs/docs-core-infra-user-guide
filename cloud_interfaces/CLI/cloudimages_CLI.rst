.. _cloudimages_CLI:

-----------------------------
Cloud Images and CLIs: glance
-----------------------------
To interact with Cloud Images at the command line, 
you can use tools created specifically for the purpose 
of interacting with OpenStack-based clouds 
(nova, glance) 
or general-purpose tools (cURL). 

Because Cloud Servers and Cloud Images work so 
closely together, 
the command-line tools that work well with Cloud Servers 
also work well with Cloud Images. 

You can read about these as a group at 
:ref:`cloudservers_CLI` 
or you can go directly to the tool that interests you:

* :ref:`nova`
* :ref:`supernova`
* :ref:`curl`

You can also use the 
:ref:`cinder`, 
focused on Cloud Images. 

In working with Cloud Images, 
you may find that you need to use nova for some functions 
and glance for others. You should install them both. 
You can see an example of using nova and glance together at 
`Openstack CLI Basics <https://developer.rackspace.com/blog/openstack-cli-basics/>`__ 
where, in the "Creating a Modified Image" section, 
``glance image-create`` establishes a new image 
and ``nova boot`` initializes a new server from that image. 

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
`API cross-reference <http://api.rackspace.com/api-ref-images.html>`__ 
lists those requests for Cloud Images.  
 
The Getting Started Guide for the Cloud Images API 
includes many examples of using cURL commands 
to send requests to the API's endpoint, 
especially at 
`Using images <http://docs.rackspace.com/images/api/v2/ci-gettingstarted/content/using-images.html>`__.
  
The Developers Guide for the Cloud Images API 
also demonstrates using cURL to interact with the API, such as at 
`How cURL commands work <http://docs.rackspace.com/images/api/v2/ci-devguide/content/curl_stuff.html>`__.
  
Contents:

.. toctree::
   :maxdepth: 2  

   glance 
