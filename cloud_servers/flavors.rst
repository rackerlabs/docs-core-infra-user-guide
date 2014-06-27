Creating Servers: Flavors and Flavor Classes
=============================================

In Rackspace Cloud Servers, built on OpenStack, there are two concepts 
that help organize different virtual or physical machine characteristics to help 
you make logical decisions about the type of servers you need to create: Flavors and Flavor Classes.

Flavors
-------
    
A "flavor" is the definition of the characteristics and resources that your newly created server will have assigned to it. Each flavor has an ID and description for easy reference, and a specficiation of its resources.

An example of a Flavor is the **Performance-1-1**, or "1GB Performance" server flavor. (If you use the ``nova flavor-list`` command to view a list of the Cloud Server flavors at Rackspace, you will see something similar to the following (abbreviated for easier reading)::

    +------------------+-------------------------+-----------+------+-----------+------+-------+-------------+
    | ID               | Name                    | Memory_MB | Disk | Ephemeral | Swap | VCPUs | RXTX_Factor | 
    +------------------+-------------------------+-----------+------+-----------+------+-------+-------------+
    | performance1-1   | 1 GB Performance        | 1024      | 20   | 0         |      | 1     | 200.0       | 
    +------------------+-------------------------+-----------+------+-----------+------+-------+-------------+

(When using the Cloud Control Panel or other tools, the descriptions of resources may vary slightly, but the concepts and results are the same. See XXXX for information on the various ways to view and create Cloud Servers XXXX)

We can see that the **Performance1-1** server will have the following resources assigned to it when your instance is created:

* **ID**: This is the unique identifier for the flavor, and what is used when using the ``nova`` utility or OpenStack API to specify a desired flavor. 
* **Description**: The "friendly" name for the Flavor. When talking about a Flavor (versus using utilities, APIs, or SDKs), it is not uncommon to see it referred to by the ID or the description somewhat interchangeably. 
* **Memory_MB**: The amount of RAM, specified in megabytes; in this case 1GB of available RAM. 
* **Disk** (also known as "**System disk**"): Sometimes also called "boot disk", this is simply the size of the first disk the server will attempt to access and boot from, much like the first physical hard drive plugged into a normal computer. A Performance1-1 (and indeed all Performance servers) have a 20GB System disk. *Note: if using Cloud Block Storage as your boot volume, that volume will take precedence in the boot order over the system disk. See XXX for more info* 
* **Ephemeral** (also known as "**Data disk(s)**"): Data disk space, versus the "System disk" described above, is additional disk space, spread across one or more virtual disks, available to use for your application data, caching, or other scenarios. Not all Flavors will have Data disks assigned to them; in this example, **Performance1-1** does not. In addition, there are some important things to be aware of when using your Data disks:
    * They will **not be captured** when a snapshot/image of your server is created; only the System disk is captured. Using a backup solution like Rackspace Cloud Backup or other technology is **highly recommended** if using the Data disks to store critical data.
    * Data disks may need to be formatted, partitioned, or grouped into a software RAID group, depending on your needs. The Data disks are provided as empty or raw disks in some cases to allow you maximum flexibility in how you use them.  XXXX link to info on formatting them XXXX
* **Swap**: Swap is the size of an additional partition provided to your instance that would generally be used by Linux for swap memory space. As of early 2014, a swap partition is no longer provided for most flavors, as it can degrade performance or hide memory usage issues. Rackspace recommends choosing a server flavor that will have enough RAM to support your application without the use of swap. 
* **VCPUs**: The number of virtual CPU cores that will be available. This is important when planning and deploying applications that are multi-threaded or CPU constrained. The **Performance1-1** flavor has 1 VCPU assigned.  Depending on the flavor, VCPUs may be provided exclusively to your instance, or may be shared in a time slicing fashion with other virtual machines. XXXX do we want to cover oversubscription here XXXX
* **RXTX_Factor**: The amount of aggregate outbound bandwidth across all attached networks on your Cloud Server (PublicNet, ServiceNet, Cloud Networks). *(For more information on the different networks available to your Cloud Server, see XXXXX section.)* Maximum outbound public bandwidth is limited to 40% of the aggregate, while inbound traffic is not limited. In the case of **Performance1-1**, this means that you would be able to generate 80Mb/s (Megabits per second) of outbound traffic/bandwidth. 

These resources are fixed: i.e. you can not create a server and then change the amount of RAM available to it (or disk, CPU, etc.). To change to a server with a different set of resources ("Flavor"), you will need to create a new server and migrate any applications and/or data to it. 

Flavor Classes
--------------

A Flavor Class is simply a grouping of Flavors based on similar characteristics to help make easier decisions around technology choices, resources, or pricing models. Common Flavor Classes at Rackspace are:

* **Performance 1**: An entry level, high performance virtual server, with up to 8GB of RAM, 8 virtual CPU, and 40GB system/80GB data SSD disk space. There is limited oversubscription of the CPU resources on Performance 1. XXX link to oversubscription XXX

* **Performance 2**: Performance 2 continues the use of high performance SSD storage, and extends resources up to 120GB of RAM, 32 virtual CPU, and 40GB system/1.2TB data disk space. 

* **Standard** (*Also referred to as Standard 1*): The Standard Flavor Class was originally launched with the Rackspace Next Generation Cloud in 2012. Although available in some scenarios, Rackspace recommends using a Performance or other flavor class which generally provides greater performance and value for an overall lower price. Standard flavors provide up to 30GB RAM, 8 virtual CPU, and 1.2TB of SATA (non-SSD) disk. 

* **OnMetal placeholder**

If we revisit the ``nova flavor-list`` command output, we can see a more full picture of the different Flavor Classes available:: 

    +------------------+-------------------------+-----------+------+-----------+------+-------+-------------+-----------+
    | ID               | Name                    | Memory_MB | Disk | Ephemeral | Swap | VCPUs | RXTX_Factor | Is_Public |
    +------------------+-------------------------+-----------+------+-----------+------+-------+-------------+-----------+
    | 2                | 512MB Standard Instance | 512       | 20   | 0         | 512  | 1     | 80.0        | N/A       |
    | 3                | 1GB Standard Instance   | 1024      | 40   | 0         | 1024 | 1     | 120.0       | N/A       |
    | 4                | 2GB Standard Instance   | 2048      | 80   | 0         | 2048 | 2     | 240.0       | N/A       |
    | 5                | 4GB Standard Instance   | 4096      | 160  | 0         | 2048 | 2     | 400.0       | N/A       |
    | 6                | 8GB Standard Instance   | 8192      | 320  | 0         | 2048 | 4     | 600.0       | N/A       |
    | 7                | 15GB Standard Instance  | 15360     | 620  | 0         | 2048 | 6     | 800.0       | N/A       |
    | 8                | 30GB Standard Instance  | 30720     | 1200 | 0         | 2048 | 8     | 1200.0      | N/A       |
    | performance1-1   | 1 GB Performance        | 1024      | 20   | 0         |      | 1     | 200.0       | N/A       |
    | performance1-2   | 2 GB Performance        | 2048      | 40   | 20        |      | 2     | 400.0       | N/A       |
    | performance1-4   | 4 GB Performance        | 4096      | 40   | 40        |      | 4     | 800.0       | N/A       |
    | performance1-8   | 8 GB Performance        | 8192      | 40   | 80        |      | 8     | 1600.0      | N/A       |
    | performance2-120 | 120 GB Performance      | 122880    | 40   | 1200      |      | 32    | 10000.0     | N/A       |
    | performance2-15  | 15 GB Performance       | 15360     | 40   | 150       |      | 4     | 1250.0      | N/A       |
    | performance2-30  | 30 GB Performance       | 30720     | 40   | 300       |      | 8     | 2500.0      | N/A       |
    | performance2-60  | 60 GB Performance       | 61440     | 40   | 600       |      | 16    | 5000.0      | N/A       |
    | performance2-90  | 90 GB Performance       | 92160     | 40   | 900       |      | 24    | 7500.0      | N/A       |
    +------------------+-------------------------+-----------+------+-----------+------+-------+-------------+-----------+
  
*Note 1:In this case, the Flavors are not specifically shown as being grouped into Flavor Classes, but they can be inferred by the ID or other information. In the Cloud Control Panel, and on Rackspace.com, Flavor Classes will typically be broken out by the definitions mentioned above.*
  
*Note 2:The "Is_Public" column is an OpenStack feature that does not need to be considered when evaluating your flavor class decisions.*

Choosing the right Flavor Class 
-------------------------------

Flavor Classes and Flavors are often defined and grouped such that they provide meaningful guidance in selecting the right choice for your workload or application. The process of choosing the right Flavor Class and Flavor is generally analogous to choosing the resources and specifications you would for physical hardware. 

Some examples are:

* **Web servers and other horizontally scaling application tiers**: As web servers, such as Apache or Nginx, typically derive their performance from network bandwidth, and to a lesser extent CPU and RAM, versus disk space, choosing a **Performance 1** flavor can often be the right decisions. It has ample network bandwidth, and CPU and RAM allocations that often match today's highly optimized web server applications.
* **Database servers**: These servers, whether SQL or NoSQL, often benefit from very fast disk, and moderate to substantial amounts of RAM and CPU resources. While these servers can be both vertically and horizontally scaled in different scenarios, the application resources needed can often remain significant. In these cases, **Performance 2** might be a good choice.

* **OnMetal placeholder**


Ultimately, choosing a Flavor Class and Flavor comes down to understanding your application needs (both now and in the future), and balancing that against the amount and type of resources it will need. 

Region Availability for Flavor Classes
--------------------------------------

Rackspace Cloud Servers are available to be created/consumed in multiple regions (XXX link to description of regions wherever that is XXX). However, not all Flavor Classes and Flavors may be available in all regions. When choosing a Flavor Class & Flavor, be sure to check the available flavors for your region via the ``nova flavor-list`` command, the Cloud Control Panel, or information on Rackspace.com. 

    •   Performance dashboard (future)  <-- not sure what this is....