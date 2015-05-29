.. _cloudnetworks_CLI:

--------------------------------
Cloud Networks and CLIs: neutron
--------------------------------
To interact with Cloud Networks at the command line, 
you can use tools created specifically for the purpose 
of interacting with OpenStack-based clouds 
(nova, neutron) 
or general-purpose tools (cURL). 

Because Cloud Servers and Cloud Networks work so 
closely together, 
the command-line tools that work well with Cloud Servers 
also work well with Cloud Networks. 

You can read about these as a group at 
:ref:`cloudservers_CLI` 
or you can go directly to the tool that interests you:

* :ref:`nova`
* :ref:`supernova`
* :ref:`curl`

You can also use the 
:ref:`neutron`, 
focused on Cloud Images.

In working with Cloud Networks, 
you may find that you need to use nova for some functions 
and neutron for others. You should install them both. 
You can see an example of using nova and neutron together at 
xxxxxxxx find example 
`Openstack CLI Basics <https://developer.rackspace.com/blog/openstack-cli-basics/>`__ 
where, in the "Creating a Modified Image" section, 
``glance image-create`` establishes a new image 
and ``nova boot`` initializes a new server from that image. xxxxxxxx


Before you can use one of these tools, 
you must install a local (client) copy. 
The installation procedure varies for each tool 
and is documented with the tool. 

The commands you can send are the 
the same, 
wrapped in the syntax of the client, 
as the requests you can send 
to the API endpoint. 
http://api.rackspace.com/api-ref-networks.html 
lists those requests for Cloud Networks. 

The Getting Started Guide for the Cloud Networks API 
includes detailed, parallel examples showing how you can use 
either
cURL or neutron to perform the same functions. 
If you compare the matching cURL and neutron examples, 
you can see how these tools differ and why you might 
prefer to work with one or the other. 
For example, if you compare 
`Create a network (neutron client) <http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/neutron_create_network_chr_neutron.html>`__, 
and 
`Create a network (cURL) <http://docs.rackspace.com/networks/api/v2/cn-gettingstarted/content/neutron_create_network_chr_curl.html>`__  
you can see that:

* neutron  users send ``neutron net-create Rackernet``
* cURL users send ``$ curl -s https://dfw.networks.api.rackspacecloud.com/v2.0/networks \
  -X POST \
  -H "Content-Type: application/json" \
  -H "User-Agent: python-novaclient" \
  -H "Accept: application/json" \
  -H "X-Auth-Token: $token" \
  -d '{"network": {"name": "Rackernet"}}' | python -m json.tool`` 

Contents:

.. toctree::
   :maxdepth: 2  

   neutron  