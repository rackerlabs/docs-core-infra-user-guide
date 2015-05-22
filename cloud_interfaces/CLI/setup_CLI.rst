.. _setup_CLI:

----------------------
Preparing to use a CLI
----------------------
To interact with the Rackspace cloud at the command line,  
you must have the same basic things you need 
if you wish to interact via the Cloud Control Panel 
or via an SDK or API:

* a Rackspace cloud account
* credentials enabling access to that account

  * username and password allow you to login to the Cloud Control Panel
  * after you login, you can obtain your API key 
    and your tenant ID (also called account number)

Working through a CLI is different from working through a GUI or API 
in one important way: you must install a local client. 

* To send requests via a GUI such as the Cloud Control Panel, 
  you use the Web browser 
  installed on your machine to interact with a Web server operated by 
  Rackspace. The Web server interacts with the API endpoint on your 
  behalf. 
  
* To send requests via an API, you write your own software to 
  interact with an API endpoint operated by Rackspace. 
  
* To send requests via a CLI, you download and install appropriate 
  client software, then use that software to interact with an 
  API endpoint operated by Rackspace. 

Beyond this general process, the details vary 
depending on which service you are working with. 
For product-specific introductions to 
the CLIs relevant to specific 
core infrastructure products, see

* :ref:`cloudservers_CLI`
* :ref:`cloudnetworks_CLI`
* :ref:`cloudimages_CLI`
* :ref:`cloudblockstorage_CLI`