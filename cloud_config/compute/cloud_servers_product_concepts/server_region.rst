.. _server _region:

^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Creating a Cloud Server in a region
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
When you plan to build a Cloud Server, you may be interested in the
geographical region of its physical host. Choosing the right region can
optimize network delivery speed for local users. For example, if you
expect most of the Cloud Server's workload to originate in Australia,
you may prefer it to be hosted in our SYD region rather than in our DFW
region.

Beyond a general preference for a region, though, working in the cloud
means that you need not be concerned with selecting among the hundreds
or thousands of physical servers available in that region.

When you request creation of a new Cloud Server, your request describes
the initial resources you want to make available to that Cloud Server.
We use that description to choose an appropriate physical host for your
Cloud Server.

* If you use the Cloud Control Panel to create your new Cloud Server,
  you describe your requirements by choosing a region, an image, and a
  flavor class, and then moving the slider up toward the maximum or
  down toward the minimum resource levels for that class.

* If you use an SDK, you begin describing your new Cloud Server by
  authenticating at an API endpoint (which identifies a region), and
  then choosing an image and a flavor, as shown at
  `Quickstart for Cloud Servers <https://developer.rackspace.com/docs/cloud-servers/getting-started/>`__.

No matter how you submit your request to create a Cloud Server, the
resources described in the request determine the placement of your Cloud
Server on a physical host capable of providing those resources. For
example, the three figures below demonstrate using the Cloud Control
Panel to describe the resources needed for a 1 GB standard instance of a
cloud server in the standard flavor class, running Ubuntu in the DFW
region.

***Step 1: Server Details***

Choose a region that is near many of your users, reducing their network
transfer time.

.. figure:: /_images/CloudServerCreateRegionDFW.png
   :alt: Choose a region.  
         Your choice can affect network delivery speed.
         
   *Choose a region. 
   Your choice can affect network delivery speed.*

***Step 2: Image***

Choose an image that supports the applications you intend to run.

.. figure:: /_images/CloudServerCreateImageUbuntu.png
   :alt: Choose an operating system. 
         Your choice can affect your cost.
         
   *Choose an operating system. 
   Your choice can affect your cost.*

***Step 3: Flavor***

Choose a flavor that offers adequate capacity and the price you want to
pay. Moving the blue slider up and down changes initial resource sizes;
hovering over the green circle pops up an explanation of pricing.

.. figure:: /_images/CloudServerCreateFlavorStandardInstance.png
   :alt: Choose resource sizes. 
         Your choice can affect your cost.
   
   *Choose resource sizes. 
   Your choice can affect your cost.**

After you submit your request, nova-scheduler, the component responsible
for appropriately assigning a new Cloud Server to a physical host,
compares two sources of information:

* your detailed server-creation request

* details describing the current capacity of physical hosts available
  in the region you selected

Nova-scheduler then places your server on a physical host capable of
providing the resources you described.

By default, nova-scheduler does not place multiple Cloud Servers
belonging to the same account on the same physical host. However, it is
possible to override this default in some circumstances. Every Cloud
Server has a *Host ID*, identifying its physical host; by examining the
*Host ID* for each Cloud Server, you can determine whether any of your
Cloud Servers have been placed on the same physical host.
