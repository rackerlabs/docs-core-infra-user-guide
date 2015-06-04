.. _create_server:

---------------------------------------------
Using flavors to configure a new Cloud Server
---------------------------------------------
When you create a Cloud Server, you choose its basic configuration by
selecting from the available *flavors*; similar flavors are grouped as
*flavor classes*.

A flavor is the definition of the characteristics and resources that are
assigned to a Cloud Server when it is created.

For example, you can create a 1GB Cloud Server by selecting the
**General Purpose** flavor class and the **1 GB General Purpose v1**
flavor. By making one choice of a flavor, you create a server with the
following characteristics:
 

+++++++++ 
Flavor ID 
+++++++++ 
The flavor's unique identifier, ``ID``, 
is used in the API to specify a desired flavor.
       
For example, ``general1-1``.
     
Flavor IDs are returned by 
the *List Flavors* API operation, 
described in the 
`Cloud Servers API documentation <http://docs.rackspace.com/servers/api/v2/cs-devguide/content/List_Flavors-d1e4188.html>`__.
 
++++++++++++++++++
Flavor description
++++++++++++++++++       
``description`` is the friendly name for the flavor. 
     
For example, ``1 GB General Purpose v1``.

+++++++++++++
Flavor memory
+++++++++++++
``memory`` is the amount of RAM, available to this flavor, 
specified in megabytes. 
     
For example, 1GB of available RAM.

+++++++++++++++++++++++++
Flavor disk / system disk
+++++++++++++++++++++++++
Sometimes also called boot disk, 
``flavor disk / system disk`` describes 
the size of the first disk that 
the server will attempt to access and boot from, 
much like the first physical hard drive 
plugged into a physical computer. 
     
For example, a ``general1-1`` server 
has a 20GB system disk.

+++++++++++++++++++++
Ephemeral / data disk
+++++++++++++++++++++
Data disk space, versus *system* disk space, 
is additional disk space spread across one or more virtual disks, 
available to use for application data, caching, 
or other scenarios.
     
Not all flavors have data disks assigned to them. 
For example, the ``general1-1`` flavor provides no data disk.
     
In addition, there are some important things to be aware of 
when using data disks:
     
* Data disks are not captured when a snapshot/image 
  of your server is created; only the system disk is captured. 
  Using a backup solution such as Rackspace Cloud Backup 
  is highly recommended if you use 
  data disks to store critical data.
       
* Data disks may need to be formatted, partitioned, 
  or grouped into a software RAID group. 
  The data disks are provided as empty or raw disks 
  in some cases to allow you maximum flexibility in using them.

++++
Swap
++++
Swap is the size of an additional partition provided 
to your instance that would generally be used by Linux 
for swap memory space. 

Rackspace does not provide a swap partition for most flavors, 
as it can degrade performance or hide memory usage issues. 
     
Rackspace recommends choosing a server flavor with enough RAM 
to support your application without the use of swap.

+++++
vCPUs
+++++
``vCPUs`` is the number of virtual CPU cores 
available to this flavor. 
This is important when planning and deploying applications 
that are multi-threaded or CPU constrained. 

For example, the ``general1-1`` flavor has 1 vCPU assigned.
     
Depending on the flavor, 
vCPUs may be provided exclusively to your instance, 
or may be shared in a time-slicing fashion 
with other virtual machines.

+++++++++++
RXTX factor
+++++++++++
The amount of aggregate outbound bandwidth across 
all attached networks (PublicNet, ServiceNet, Cloud Networks)
on your Cloud Server. 
     
For more information on the different networks 
available to your Cloud Server, 
see 
:ref:`network_cloud_servers-working`.

Maximum outbound public bandwidth is limited to 40% 
of the aggregate, while inbound traffic is not limited. 
In the case of the ``general1-1`` flavor, 
aggregate bandwidth of 200Mb/s 
(Megabits per second) means that you can 
generate 80Mb/s of outbound traffic.
