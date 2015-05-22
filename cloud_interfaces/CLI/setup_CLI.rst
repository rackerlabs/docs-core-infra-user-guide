.. _setup_CLI:

----------------------
Preparing to use a CLI
----------------------
To interact with the Rackspace cloud at the command line,  
you must have some of the same things you would need 
if you wished to interact by choosing options on a Web page 
(:ref:`the Cloud Control Panel <cloud_interfaces_GUI>`) 
or by writing software 
(:ref:`SDK or API <cloud_interfaces_API>`):

* a Rackspace cloud account
* credentials enabling access to that account

  * username and password allow you to login to the Cloud Control Panel
  * after you login, you can obtain your API key 
    and your tenant ID (also called account number)

You also need to know something that you would need to know if working 
with an API: 

* the endpoint for the cloud service with which you want to interact

.. note::
   :ref:`setup_API` provides more detail about these prerequisites.

Beyond what you would need to use with the Control Panel or an API, 
you must have two additional tools to enable you to interact with 
the cloud by typing commands:

* a terminal emulator such as 
  `iTerm2 <https://www.iterm2.com/>`__ 
  or 
  `PuTTY <http://www.chiark.greenend.org.uk/~sgtatham/putty/>`__ 

* a locally-installed client capable of interacting with 
  the cloud service you have chosen
  
  * you can use 
    `cURL <http://curl.haxx.se/>`__ 
    to send commands to any API endpoint
  * you can use 
    `OpenStack CLIs <http://docs.openstack.org/cli-reference/content/>`__
    to send commands to specific
    cloud services

In your terminal emulator, 
you can type commands to the client and, 
if you are properly authenticated, 
the client forwards your requests to the cloud service and forwards 
the service's responses to you. 

To preserve a series of commands so that they can be easily
re-executed, 
you can place them within a 
`script <http://www.tldp.org/LDP/Bash-Beginners-Guide/html/sect_02_01.html>`__. 
To schedule automated execution of your script, you can 
invoke it from a 
`cron job <http://www.unixgeeks.org/security/newbie/unix/cron-1.html>`__.  

Beyond this general process, the details vary 
depending on which service you are working with. 
For product-specific introductions to 
the CLIs relevant to specific 
core infrastructure products, see

* :ref:`cloudservers_CLI`
* :ref:`cloudnetworks_CLI`
* :ref:`cloudimages_CLI`
* :ref:`cloudblockstorage_CLI`