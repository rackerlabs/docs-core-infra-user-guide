Installing a software stack
---------------------------
When you create a Cloud Server, unless you begin from an existing
Cloud Images configuration, only an operating system is installed. You
can then install any additional software that is compatible with the
Cloud Server's configuration.

You can install software manually, following the software provider's
instructions. Before you can run some software, you'll have to install a
set of enabling software; for example, if you want to publish a blog
using the WordPress content management system, you'll have to provide
WordPress with a Linux+Apache+MySQL+PHP environment (LAMP stack). To see
this multi-step process, watch the videos at
https://launch.rackspace.com/guides/wordpress.

For many popular software packages and their enabling stacks, Rackspace
offers an easier way. When you create a Cloud Server, you can choose to
install specific software in addition to the operating system. To do
that through the Cloud Control Panel, choose "Create Stack" rather than
"Create Server", then choose a template describing the software you want
to install. We frequently expand the list of templates; as of February
19, 2015, these templates are available:

• Ansible Tower

• ASP .Net

• Cassandra

• Chef Server

• Django

• DNN

• Docker

• Drone.io

• Drupal

• Elasticsearch

• Ghost

• GitLab

• Graphite

• IPython Notebook

• JabbR

• Jenkins

• LAMP

• Magento

• memcached

• Minecraft

• MongoDB

• MySQL

• Node.js

• ownCloud

• PHP

• Rails

• Redis

• SaltStack

• StrongLoop

• Umbraco

• Vesta

• WebPageTest

• WordPress

If you've written your own automation to create Cloud Servers, you can
use the Cloud Orchestration API to create a server from one of our
templates. You can also use the API to create your own templates and
then use one of your own templates to create your own Cloud Servers. You
can learn about the Cloud Orchestration API at
http://docs.rackspace.com/.

Because installing and customizing software can be time-consuming, it's
a good idea to save a copy of a Cloud Server that already has the
software you need, configured just the way you like it. You can use
Cloud Images to maintain a consistent starting point for future Cloud
Servers you create.
