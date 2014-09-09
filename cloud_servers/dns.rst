DNS
===

Reverse DNS
-----------

For each Cloud Server you create, you can assign a Reverse DNS record. A
Reverse DNS record is also known as a "PTR record", and is used to assist in
the resolution of a specific IP to a fully qualified domain name (FQDN), like
mail.example.com. 

How Reverse DNS works
^^^^^^^^^^^^^^^^^^^^^

When you enter a domain name into your browser, the DNS system will find the IP
address of the server the domain is associated with.

A reverse DNS lookup does the opposite. It establishes what domain is
associated with the IP address. 

Reverse DNS importance with hosted mail servers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Reverse DNS is especially important if you are running an
application like a mail server on your Cloud Server, as many recipient servers
reject, or mark as spam, all email that originates from an “unauthenticated”
server.

This basically means that after the sending IP address is checked, if the
reverse DNS does not match the sending domain, then it is classed as
“unauthenticated”.

Note: We put ”unauthenticated” in quotes because having a Reverse DNS record
attached to your domain does not automatically guarantee acceptance of email
originating from your domain by the recipient's email server. It's just that
non-matching or generic reverse DNS lookup settings are often rejected out of
hand. Having a reverse DNS record for your domain will prevent email
originating from your domain from getting immediately rejected.

Creating your Cloud Server Reverse DNS record
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can easily set up reverse DNS through the Rackspace Cloud Control Panel. Just perform these
steps:

1. Log in to your Rackspace account.
2. On the Servers tab, click the link for your Cloud Server from your Servers
List.
3. On the Server Details screen, click Add Recordnext to the Reverse DNS option.

[insert corresponding screenshot from
http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-creating-a-reverse-dns-record]

4. In the resulting window:

* Enter you domain name (for example “mail.example.com”) in the Hostname field.
* Set the Time to Live (TTL) for the record.
* Click *Save Record*.

Now, on the Server Details screen, you will now see 1 Record listed next to the
Reverse DNS option. Clicking this link will display the details for the reverse
DNS you just added.

Troubleshooting your Reverse DNS record
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

A handy tool called *dig* can be used to troubleshoot or verify your Reverse
DNS record if you're having issues. A helpful Knowledge Center article covering
this can be found at:
http://www.rackspace.com/knowledge_center/article/rackspace-cloud-essentials-using-dig-for-dns-verification-and-troubleshooting


Forward DNS
-----------
