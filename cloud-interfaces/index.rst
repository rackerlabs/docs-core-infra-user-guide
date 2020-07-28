.. _cloud-interfaces:

==========================
Interacting with the cloud
==========================
One benefit of having a cloud based on open standards,
designed for
consistency and ease of use,
is that there are multiple ways to interact with
and manage your cloud resources.

The Rackspace cloud provides Application Programming Interfaces
(APIs) based on OpenStack for all of its management functionality.
The APIs provide direct programmatic access to cloud services,
and they also
power the Cloud Control Panel (GUI) and the command-line interfaces (CLIs).

Depending on your needs,
you might want to interact with the cloud through
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
  you use a web browser
  installed on your computer to interact with a web server operated by
  Rackspace. The web server interacts with the API endpoint on your
  behalf.

* To send requests via a CLI, you download and install appropriate
  client software on your computer, and then use that software
  within a terminal emulator to interact with an
  API endpoint operated by Rackspace.

* To send requests via an API, you write your own software to
  interact with an API endpoint operated by Rackspace.

.. toctree:: :hidden:
   :maxdepth: 6

   gui/index
   cli/index
   api/index
