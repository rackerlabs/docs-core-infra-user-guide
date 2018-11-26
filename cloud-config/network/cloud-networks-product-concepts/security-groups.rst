.. _security-groups:

~~~~~~~~~~~~~~~
Security groups
~~~~~~~~~~~~~~~

A security group is a named container for security group rules.
Security group rules provide Rackspace Public Cloud users the ability
to specify the types of traffic that are allowed to pass
through, to, and from ports on a cloud server.

Security groups are available to all customers through the Cloud
Control Panel. Security Groups are available for PublicNet and ServiceNet,
but not for Cloud Networks because Cloud Networks are already isolated by tenant.

To work with security groups,
use one of the following portals:

- :ref:`neutron CLI <neutron>`
- :ref:`Cloud Networks API <cloudnetworks-api>`

Actions related to managing security groups
are listed in
:ref:`cloud-networks-product-actions`.
You can read full details about API operations
related to security groups in the
Cloud Networks API documentation under
`Security groups operations <https://developer.rackspace.com/docs/cloud-networks/v2/api-reference/sec-group-operations>`__.

To learn more about security groups, read
:how-to:`Security groups FAQ <cloud-networks-faq>` and
:rax-docs:`Use security groups to control traffic <cloud-networks/v2/getting-started/controlling-network-access/security-groups>`.

.. include:: /_common/seealso-concepts-cloud-networks.txt
