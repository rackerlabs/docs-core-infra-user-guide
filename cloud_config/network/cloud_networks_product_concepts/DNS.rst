.. _cloud_networks_DNS:

^^^^^^^^^^^^^^^^
DNS in the Cloud
^^^^^^^^^^^^^^^^
When you create a Cloud Server, it is assigned an IP address. You can
access the server by its IP address, but you may prefer to associate the
IP address with a domain name such as ``www.example.com`` 
and access the
server by that name. 
You can connect and IP address and a domain name in
two ways:

* Use forward DNS to match a domain name to an IP address.

* Use reverse DNS to map an IP address to a domain name.

Forward DNS
'''''''''''
Most DNS lookups are forward DNS lookups, in which a search is based on
the DNS name of another computer as it is stored in a host (A) resource
record. For example, when you ask your web browser to display
``www.example.com``, you are asking for a forward DNS lookup. To enable
users to locate your Cloud Server by forward DNS lookup, register a
domain name, using the registrar of your choice. Then associate the
domain name with the Cloud Server's IP address. You can use Cloud DNS to
associate a domain name with a Cloud Server. In the Cloud Control Panel,
select Networking > Cloud DNS > Create Domain:

.. figure:: /_images/CloudDNSCreateDomain.png
   :alt: Networking > Cloud DNS > Create Domain
   
   *Networking > Cloud DNS > Create Domain*

For more about using the Cloud Control Panel to manage DNS information,
read
`Create DNS Records for cloud servers with the Control Panel <http://www.rackspace.com/knowledge_center/article/creating-dns-records-for-cloud-servers-with-the-control-panel>`__.

You can also use the Cloud DNS API to manage DNS information
programmatically. Begin reading about that in the 
`Cloud DNS API Getting Started Guide <http://docs.rackspace.com/cdns/api/v1.0/cdns-getting-started/>`__.

Reverse DNS
'''''''''''
For each Cloud Server you create, you can assign a reverse DNS record. 
A reverse DNS record, also known as a PTR record, 
is used to
assist in the resolution of a specific IP to a fully-qualified domain
name (FQDN) such as ``mail.example.com``.

When you enter a domain name into your browser, the DNS system finds the
IP address of the server the domain is associated with.

A reverse DNS lookup works in the opposite direction. 
It establishes
which domain is associated with the IP address.

Reverse DNS importance with hosted mail servers
----------------------------------------------- 
Reverse DNS is especially important if you are running an application
like a mail server on your Cloud Server, as many recipient servers
reject, or mark as spam, all email that originates from an
"unauthenticated" server.

This basically means that after the sending IP address is checked, if
the reverse DNS does not match the sending domain, 
then it is classed as
"unauthenticated".

.. NOTE:: 
   We put "unauthenticated" in quotes because having a reverse DNS
   record attached to your domain does not automatically guarantee
   acceptance of email originating from your domain by the recipient's
   email server. 
   Having a reverse DNS record for your domain can prevent
   email originating from your domain from being immediately rejected.
   Non-matching or generic reverse DNS lookup settings 
   are often rejected
   out of hand, but rejection can occur for other reasons.

Creating a Reverse DNS record for your Cloud Server
--------------------------------------------------- 
You can set up a reverse DNS through the Rackspace Cloud Control
Panel by performing these steps:

1. Log in to your Rackspace account.

2. On the Servers tab, click the link for your Cloud Server from your
   Servers List.

3. On the Server Details screen, click Add Record next to the Reverse
   DNS option.

.. figure:: /_images/CloudDNSAddReverse.png
   :alt: Servers > Server Details > Add Record
   
   *Servers > Server Details > Add Record*

4. In the resulting window:

* Enter your domain name (for example ``mail.example.com``) in the
   Hostname field.

* Set the Time to Live (TTL) for the record.

* Click *Save Record*.

After you have done this, on the Server Details screen, you will see
one record listed next to the Reverse DNS option. Clicking this link
displays the details for the reverse DNS you just added.

.. figure:: /_images/CloudDNSAddReverseDetails.png
   :alt: Servers > Server Details > Add Record
   
   *Servers > Server Details* 

Troubleshooting your reverse DNS record
---------------------------------------
If you need to verify or troubleshoot your reverse DNS record, you can
use a tool called *dig*. You can learn more about *dig* at
`Rackspace Cloud Essentials - Using dig for DNS Verification and Troubleshooting <http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-using-dig-for-dns-verification-and-troubleshooting>`__.
