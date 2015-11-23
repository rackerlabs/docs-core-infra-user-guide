.. _custom-images:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Creating custom images from servers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The first time that you boot a cloud server, you’ll probably use an image
supplied by Rackspace. We supply images of many different operating
systems, all configured to run optimally in the Rackspace cloud.

Because the images supplied by Rackspace need to appeal to a wide range of
customers with varying use cases, you might find that you have to
manually install some of the packages that your applications require, and
you might have unique configuration needs. For example, you might prefer to
run httpd on port 8080 instead of its default port 80. If you have only
one server, such customization might not be an issue,
but if you’re using the cloud, you might find that you
need to scale horizontally by creating more servers of the same kind.

There are two general approaches that you can take for this task:
bootstrapping and baking.

* **Bootstrapping**: Whenever you need a new server, use a Rackspace
  base image to boot your server and then use a configuration
  management tool such as Chef or Puppet to install the extra packages
  and make the appropriate configuration changes.

* **Baking**: Use a Rackspace base image to boot your first server.
  Then install your packages on the server, make the appropriate
  configuration changes. When the server is set up
  properly, create an image of the server. Then when you need to scale
  horizontally, you can use the image to boot the new servers, which
  will contain all of your customizations.

Each approach has advantages and disadvantages. Which one you pick
depends on your application and workflow needs.

* With bootstrapping, your cloud server is likely to boot quickly.
  Because so many users utilize the Rackspace base images, they tend to
  be cached close to most hypervisors and download quickly. After the
  server initializes, you must run your configuration
  management tool to install the software and modify the server before
  it is ready for your application.

* With baking, as soon as your cloud server initializes, everything is
  installed and configured, so your application should be ready to use.
  Because you’re using your own private virtual machine image, however,
  it’s unlikely that the image is cached anywhere, and it might take
  longer to download your image from Cloud Images to the host machine
  where your server will be built.

It’s also possible to combine the two approaches. Many people use
bootstrapping to prepare and test a server, and then they bake an image
of that server to use for deployments. One advantage to the combined
approach is that you can benefit from
updates Rackspace makes to its base images. For example, when a base
image is updated to address a security vulnerability, you can use your
bootstrapping tools to prepare an updated image of your particular
application server.

.. include:: /_common/seealso-concepts-cloud-images.txt
