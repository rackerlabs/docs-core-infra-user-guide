.. _stack:

---------------------------
Installing a software stack
---------------------------
When you create a cloud server, unless you begin from an existing
Cloud Images configuration, only an operating system is installed. You
can then install any additional software that is compatible with the
server's configuration.

You can install software manually, following the software provider's
instructions. Before you can run some software,
you'll have to install a
set of enabling software; for example, if you want to publish a blog
using the WordPress content management system, you'll have to provide
WordPress with a Linux+Apache+MySQL+PHP environment
(a **LAMP** stack).
To learn about
this multi-step process, perform the following actions:

* Read the following articles about LAMP stacks:

  * :kc-article:`Install a LAMP stack on Ubuntu or Debian <install-a-lamp-stack-on-ubuntu-or-debian>`

  * :kc-article:`How to Install a LAMP stack on CentOS, Fedora, or Red Hat <how-to-install-a-lamp-stack-on-centos-fedora-or-red-hat>`

  * :kc-article:`Migrating an Application Built on a LAMP Stack from Amazon Web Services <migrating-an-application-built-on-a-lamp-stack-from-amazon-web-services>`

* Complete the Cloud Launch Guide tutorial for
  `CMS with WordPress <https://launch.rackspace.com/guides/wordpress>`__

For many popular software packages and their enabling stacks, Rackspace
offers an easier way to get what you need. When you create a server,
you can choose to
install specific software in addition to the operating system. To do
that through the Cloud Control Panel, choose **Create Stack** rather than
**Create Server**, and then choose a template that describes
the software that you want
to install. We frequently expand the list of templates; as of
July 24, 2015,
the following templates are available:

.. raw:: html
   :file: stacks-from-control-panel.html

.. This list is from the control panel;
   when I update the list here, I also update it at
   http://www.rackspace.com/knowledge_center/article/available-templates-for-cloud-orchestration.

For some templates, you can choose a flavor.
For example, the Rails template is available in
single-server and multi-server flavors.

.. figure:: /_images/cloudorchestrationrailsflavors.png
   :alt: Some templates are offered in multiple flavors.

   *Some templates are offered in multiple flavors.*

If you've written your own automation to create cloud servers, you can
use the Cloud Orchestration API to create a server from one of our
templates. You can also use the API to create your own templates and
then use one of your own templates to create your own cloud servers.
To learn how to use the Cloud Orchestration API, begin with the
:rax-docs:`Rackspace Cloud Orchestration API Getting Started Guide <orchestration/api/v1/orchestration-getting-started/>`.

.. TIP::
   Because installing and customizing software can be time-consuming,
   it's
   a good idea to save a copy of a cloud server that already has the
   software that you need,
   configured just the way you like it.
   You can use
   Cloud Images to maintain a consistent starting point
   for future servers that you create.
