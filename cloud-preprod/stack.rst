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
To learn about this process, read the article
:how-to:`How to Install a LAMP stack on CentOS, Fedora, or Red Hat <how-to-install-a-lamp-stack-on-centos-fedora-or-red-hat>`.


For many popular software packages and their enabling stacks, Rackspace
offers an easier way to get what you need. When you create a server,
you can choose to
install specific software in addition to the operating system. To do
that through the Cloud Control Panel, choose **Create Stack** rather than
**Create Server**, and then choose a template that describes
the software that you want
to install.

We frequently update the list of templates.
To see the complete, up-to-the-minute list of templates,
log in to the :mycloud:`Cloud Control Panel <>` and click **Orchestration**.

For some templates, you can choose a flavor.
For example, the Rails template is available in
single-server and multi-server flavors.

In the Cloud Control Panel, you also have the option to click **Create Custom Template** to create your own template.

Additionally, if you've written your own automation to create cloud servers,
you can use the Cloud Orchestration API to create a server from one of our
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
