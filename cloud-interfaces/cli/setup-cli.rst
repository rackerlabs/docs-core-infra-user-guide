.. _setup-cli:

^^^^^^^^^^^^^^^^^^^^^^
Preparing to use a CLI
^^^^^^^^^^^^^^^^^^^^^^
To interact with the Rackspace cloud at the command line,
you must have some of the same things you would need
to interact by choosing options on a web page
(:ref:`the Cloud Control Panel <cloud-interfaces-gui>`)
or by writing software
(:ref:`SDK or API <cloud-interfaces-api>`):

* A Rackspace cloud account
* Credentials enabling access to that account

  * Your user name and password allow you to log in to the Cloud Control Panel.
  * After you log in, you can obtain your API key
    and your tenant ID (also called account number).

You also need to know something that you would need to work
with an API:

* The endpoint for the cloud service with which you want to interact

.. note::
   :ref:`setup-api` provides more detail about these prerequisites.

You must also have the following tools to enable you to interact with
the cloud by typing commands:

* A terminal emulator such as
  `iTerm2 <https://www.iterm2.com/>`__
  or
  `PuTTY <http://www.chiark.greenend.org.uk/~sgtatham/putty/>`__

* A locally installed client capable of interacting with
  the cloud service that you have chosen

  * You can use
    `cURL <http://curl.haxx.se/>`__
    to send commands to any API endpoint
  * You can use
    :os-docs:`OpenStack CLIs <cli-reference/content>`
    to send commands to specific
    cloud services.

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
depending on the service.
For product-specific introductions to
the CLIs relevant to specific
core infrastructure products, see the following sections:

* :ref:`cloudservers-cli`
* :ref:`cloudnetworks-cli`
* :ref:`cloudimages-cli`
* :ref:`cloudblockstorage-cli`
* :ref:`cloudfiles-cli`
