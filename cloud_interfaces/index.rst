.. _cloud_interfaces:

==========================
Interacting with the cloud
==========================
One of the benefits of having a cloud based on open standards, 
designed for
consistency and ease of use, 
is that there are multiple ways to interact with
and manage your cloud resources.

The Rackspace cloud provides 
OpenStack-based Application Programming Interfaces
(APIs) for all of its management functionality. 
These APIs are actually what
power the Cloud Control Panel (GUI), the Command Line Interfaces (CLIs), 
and Software
Development Kits (SDKs). 
The APIs themselves 
also provide direct programmatic access to cloud services.

Depending on your needs, 
you may prefer to interact with the cloud through 
a web-based control panel,
shell scripting, or 
software
integration with your current applications and workflows. 
The APIs provide full functionality, 
with a large set of widely-used functions also provided 
in the Cloud Control Panel and in CLIs. 
You can choose an interface
based on personal preference or business needs.

* To send requests via a GUI such as the Cloud Control Panel, 
  you use a Web browser 
  installed on your machine to interact with a Web server operated by 
  Rackspace. The Web server interacts with the API endpoint on your 
  behalf. 
  
* To send requests via a CLI, you download and install appropriate 
  client software on your machine, then use that software 
  within a terminal emulator to interact with an 
  API endpoint operated by Rackspace. 
  
* To send requests via an API, perhaps with the guidance of an SDK, 
  you write your own software to 
  interact with an API endpoint operated by Rackspace. 

Contents:

.. toctree::
   :maxdepth: 6  

   GUI/index
   CLI/index
   API/index
