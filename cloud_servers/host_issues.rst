Host Issues
===========
The physical host a virtual server resides on has been designed with redundancies for power, network, and disk to prevent failures to the underlying virtual servers. Despite steps taken to preserve uptime the need to restart a host for maintenance or issues is inevitable.

Whenever possible a virtual server will be Live-Migrated off it's current physical host to a new one. The Live-Migration is transparent to the user and the running virtual server. If a physical host is in a state where the virtual servers are down and Live-Migrate can not be used regular communication will be sent until the virtual server in question is up and running.