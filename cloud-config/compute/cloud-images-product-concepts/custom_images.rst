.. custom_images:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Creating custom images from servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The first time you boot a Cloud Server, you’ll probably use an image
supplied by Rackspace. We supply images of many different operating
systems, all configured to run optimally in the Rackspace Cloud.

Since the images supplied by Rackspace need to appeal to a wide range of
customers with varying use cases, you’ll probably find that there are
some packages your apps require that you have to install yourself and
you may have unique configuration needs. For example, you may prefer to
run httpd on port 8080 instead of its default port 80. If you only have
one server, this is not a big deal, but if you’re using the cloud,
there’s a good chance that your applications are the type that you may
need to scale horizontally by creating more servers of the same kind.

There are two general approaches you can take for this task:
“bootstrapping” or “baking”.

* ***Bootstrapping***: Whenever you need a new server, use a Rackspace
  base image to boot your server and then use a configuration
  management tool such as Chef or Puppet to install the extra packages
  and make the appropriate configuration changes.

* ***Baking***: Use a Rackspace base image to boot your first server.
  Then install your packages on the server, make the appropriate
  configuration changes, and when you’re sure that everything is set up
  properly, create an image of the server. Then when you need to scale
  horizontally, you use the image to boot the new servers, and each of
  them comes up with all your changes already baked in.

There are advantages and disadvantages to each of these approaches.
Which you pick really depends on your application and workflow needs.

* With bootstrapping, your Cloud Server is likely to boot quickly;
  since so many users utilize the Rackspace base images, they tend to
  be cached close to most hypervisors, and download quickly. After the
  Cloud Server initializes, you need to run your configuration
  management tool to install the software and modify the server before
  it is ready for your application.

* With baking, as soon as your Cloud Server initializes, everything is
  installed and configured, so your application should be ready to go.
  Since you’re using your own private virtual machine image, however,
  it’s unlikely that the image will be cached anywhere, and it will may
  longer to download your image from Cloud Images to the host machine
  where your server will be built.

It’s also possible to combine the two approaches. Many people use
bootstrapping to prepare and QE a server, and then after everything has
been verified they bake an image of that server to use for deployments.
One advantage to the combined approach is that you can benefit from
updates Rackspace makes to its base images. For example, when a base
image is updated to address a security vulnerability, you can use your
bootstrapping tools to prepare an updated image of your particular
application server.
