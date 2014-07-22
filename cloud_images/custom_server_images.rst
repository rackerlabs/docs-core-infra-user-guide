Creating Custom Images from Servers
===================================

The first time you boot a cloud server, you'll probably use an image supplied
by Rackspace.  We supply images of many different operating systems, all
configured to run optimally in the Rackspace Cloud.

Since the images supplied by Rackspace need to appeal to a wide range of
customers with varying use cases, you'll probably find that there are some
packages your apps require that you have to install yourself.  And you may have
unique configuration needs (for example, you may prefer to run httpd on port
90 instead of its default port 80).  If you only have one server, this is not
a big deal, but if you're using the cloud, there's a good chance that your
applications are the type that you may need to scale horizontally by creating
more servers of the same kind.

There are two general approaches you can take for this task: "baking" or
"bootstrapping".

Bootstrapping
  Whenever you need a new server, use a Rackspace base
  image to boot your server and then use a configuration management
  tool (e.g., Chef or Puppet) to install the extra packages and make
  the appropriate configuration changes.

Baking
  Use a Rackspace base image to boot your first server.  Then
  install your packages on the server, make the appropriate
  configuration changes, and when you're sure that everything is set
  up properly, create an image of the server.  Then when you need to
  scale horizontally, you use the image to boot the new servers, and
  each of them comes up with all your changes already baked in.

There are advantages and disadvantages to each of these approaches.  Which you
pick really depends on you application and workflow needs.

- With bootstrapping, the time for the server to boot is pretty quick
  (since so many users utilize the Rackspace base images, they tend to
  be cached close to most hypervisors, and download quickly), but then
  you need to run your configuration management tool to install the
  software and modify the server before it will be ready for your
  application.

- With baking, as soon as your server boots, everything is installed
  and configured already, so your application should be ready to go.
  Since you're using your own private virtual machine image, however,
  it's pretty unlikely that it will be cached anywhere, and it will
  take longer to download your image from Cloud Images to the host
  machine where your server will be built.

It's also possible to combine the two approaches.  Many people will use
bootstrapping to prepare and QE a server, and then once everything has
been verified, bake an image of that server to use for deployments.  One
advantage to the combined approach is that you can take advantage of updates
Rackspace makes to its base images.  When an image is updated (e.g., to
address a security vulnerability), you can use your bootstrapping tools to
prepare an updated image of your particular application server.

On-Demand Images
----------------

When you use the Cloud Control Panel or the Cloud Servers API to
create an image of one of your servers, you get a copy of your
server's system disk.  The image does not include any server state
stored in memory, and for Performance flavors, it will not include the
data disk(s).  Thus an on-demand image is not really a server backup.
It's more of a template that you can use to stamp out other servers
just like the one you've got.

When you create an on-demand image of your server, you need to be sure that
any running applications have their states saved to disk before you create
the snapshot.  Otherwise, these applications may not start correctly when
you boot a server from the image.  The time such applications should be 
quiesced is fairly brief and can be monitored by observing your server's
task state.  See `Using Task States With Server Imaging
<http://www.rackspace.com/knowledge_center/article/using-task-states-with-server-imaging>`_
in the Rackspace Knowledge Center for details.

Scheduled Images
----------------

In addition to on-demand images, you have the ability to enable Scheduled
Images on any servers for which the service is appropriate.  The Scheduled
Images service will automatically create a daily or weekly image of the server.
Remember that a virtual machine image is not really a backup of a server,
so whether Scheduled Images are an appropriate solution for you depends
entirely on your use case.  See the `Scheduled Images FAQ
<http://www.rackspace.com/knowledge_center/article/scheduled-images-faq>`_
in the Rackspace Knowledge Center for details.
