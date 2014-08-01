Flavors and Flavor Classes
==========================

In Rackspace Cloud Servers there are two concepts that help organize different
virtual or physical machine characteristics to help you make logical decisions
about the type of servers you need to create: Flavors and Flavor Classes.

Flavors
=======
    
A flavor is the definition of the characteristics and resources that your newly
created server will have assigned to it. Each flavor is described by an ID and
Description, along with the resource type and allocated amount of each
resource.

An example of a Flavor is the **Performance-1-1**, or "1GB Performance" server
flavor. We can see that the **Performance1-1** server will have the following
characteristics:

ID
^^

This is the unique identifier for the flavor, and what is used when using the 
API to specify a desired flavor. Ex: "performance1-1"

Description
^^^^^^^^^^^

The "friendly" name for the Flavor. Ex: "1GB Performance Server" 

Memory_MB
^^^^^^^^^

The amount of RAM, specified in megabytes; in this example, 1GB of available
RAM.

Disk / System Disk
^^^^^^^^^^^^^^^^^^

Sometimes also called "boot disk", this is simply the size of the first disk 
the server will attempt to access and boot from, much like the first physical 
hard drive plugged into a normal computer. A Performance1-1 has a 20GB System disk.

Ephemeral / Data Disk(s)
^^^^^^^^^^^^^^^^^^^^^^^^

Data disk space, versus the "System disk" described above, is additional disk 
space, spread across one or more virtual disks, available to use for your 
application data, caching, or other scenarios.
 
Not all Flavors will have Data disks assigned to them; in this example, 
**Performance1-1** does not. 

In addition, there are some important things to be aware of when using your 
Data disks:     

 - They will **not be captured** when a snapshot/image of your server is
   created; only the System disk is captured. Using a backup solution like
   Rackspace Cloud Backup or other technology is **highly recommended** if using
   the Data disks to store critical data.

 - Data disks may need to be formatted, partitioned, or grouped into a software
   RAID group, depending on your needs. The Data disks are provided as empty or
   raw disks in some cases to allow you maximum flexibility in how you use them.

Swap
^^^^

Swap is the size of an additional partition provided to your instance that would
generally be used by Linux for swap memory space. As of early 2014, a swap
partition is no longer provided for most flavors, as it can degrade performance
or hide memory usage issues. Rackspace recommends choosing a server flavor that
will have enough RAM to support your application without the use of swap.

vCPUs
^^^^^

The number of virtual CPU cores that will be available. This is important when 
planning and deploying applications that are multi-threaded or CPU constrained. 
The **Performance1-1** flavor has 1 vCPU assigned.

Depending on the flavor, vCPUs may be provided exclusively to your instance, or 
may be shared in a time slicing fashion with other virtual machines.

RXTX Factor
^^^^^^^^^^^

The amount of aggregate outbound bandwidth across all attached networks on your
Cloud Server (PublicNet, ServiceNet, Cloud Networks). *(For more information on
the different networks available to your Cloud Server, see XXXXX section.)*
Maximum outbound public bandwidth is limited to 50% of the aggregate, while
inbound traffic is not limited. In the case of **Performance1-1**, this means
that you would be able to generate 80Mb/s (Megabits per second) of outbound
traffic/bandwidth.


Changing the Flavor of your server
----------------------------------
These resources are fixed: i.e. you can not create a server and then change the
amount of RAM available to it (or disk, CPU, etc.). To change to a server with a
different set of resources ("Flavor"), you will need to create a new server and
migrate any applications and/or data to it.


Flavor Classes
--------------

A Flavor Class is simply a grouping of Flavors based on similar characteristics
to help make easier decisions around technology choices, resources, or pricing
models. Common Flavor Classes at Rackspace are:

Performance 1
^^^^^^^^^^^^^

An entry level, high performance virtual server, with up to 8GB of RAM, 
8 virtual CPUs, and 40GB system/80GB data SSD disk space. There is limited 
oversubscription of the CPU resources on Performance 1 flavors. 

Performance 2
^^^^^^^^^^^^^

Performance 2 continues the use of high performance SSD storage, and extends 
resources up to 120GB of RAM, 32 virtual CPUs, and 40GB System/1.2TB Data disk 
space.

Standard
^^^^^^^^

The Standard Flavor Class was originally launched with the Rackspace Next 
Generation Cloud in 2012. Although available in some scenarios, Rackspace 
recommends using a Performance or other flavor class which generally provides 
greater performance and value for an overall lower price. Standard flavors 
provide up to 30GB RAM, 8 virtual CPUs, and 1.2TB of SATA (non-SSD) disk.

TODO: Add OnMetal details

Choosing the right Flavor Class
===============================

Flavor Classes and Flavors are often defined and grouped such that they provide
meaningful guidance in selecting the right choice for your workload or
application. The process of choosing the right Flavor Class and Flavor is
generally analogous to choosing the resources and specifications you would for
physical hardware. Some examples are:

Web servers and other horizontally scaling application tiers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

As web servers, such as Apache or Nginx, typically derive their performance from
network bandwidth, and to a lesser extent CPU and RAM, versus disk space, 
choosing a **Performance 1** flavor can often be the right decisions It has 
ample network bandwidth, and CPU and RAM allocations that often match today's 
highly optimized web server applications.

Database servers
^^^^^^^^^^^^^^^^

These servers, whether SQL or NoSQL, often benefit from very fast disk, and 
moderate to substantial amounts of RAM and CPU resources. While these servers 
can be both vertically and horizontally scaled in different scenarios, the 
application resources needed can often remain significant. In these cases, 
**Performance 2** might be a good choice.

TODO: Discss OnMetal workload profiles

Ultimately, choosing a Flavor Class and Flavor comes down to understanding your
application needs (both now and in the future), and balancing that against the
amount and type of resources it will need.

Region Availability for Flavor Classes 
======================================

Rackspace Cloud Servers are available to be created/consumed in multiple
regions. However, not all Flavor Classes and Flavors may be available in all
regions. When choosing a Flavor Class & Flavor, be sure to check the available
flavors for your region via the Cloud Servers API, the Cloud Control Panel, or
information on Rackspace.com.