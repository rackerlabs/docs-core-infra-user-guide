.. _cloud_interfaces_GUI:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
GUI: Rackspace Cloud Control Panel
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The Rackspace Cloud Control Panel at https://mycloud.rackspace.com is
the easiest way to get started with provisioning cloud resources.

The Cloud Control Panel provides a simple, unified web based interface
that works in all major browsers. After signing up for a Cloud account
at `rackspace.com <http://www.rackspace.com/>`__, the Cloud Control panel is the first place you 
should visit to get an overview of products and services available,
create your first servers and resources, or view more information about
your Rackspace account.

The Cloud Control Panel is also where you can complete some important
first tasks:

* `obtain your API key <http://www.rackspace.com/knowledge_center/article/view-and-reset-your-api-key>`__
  for use with 
  :ref:`CLIs <cloud_interfaces_CLI>`, 
  :ref:`SDKs <SDK>`, 
  and 
  :ref:`APIs <APIdirect>`

* `create additional account users <http://www.rackspace.com/knowledge_center/article/managing-role-based-access-control-rbac>`__ 
  and give them 
  `permissions <http://www.rackspace.com/knowledge_center/article/permissions-matrix-for-role-based-access-control-rbac>`__ 
  if needed

  .. note::
     Users who do not have permission to use a feature 
     do not see that feature in the Cloud Control Panel. 
     Cloud Control Panel screenshots in the
     `Knowledge Center <http://www.rackspace.com/knowledge_center/>`__ 
     and elsewhere may show features that are not 
     available to some users.

* view and change resource limits

  .. figure:: /_images/AccountResourceLimits.png
     :scale: 80%
     :alt: Use the Control Panel to see your current
         limits and to ask to change them.
         
     Use the Control Panel to see your current
     limits and to ask to change them.
         
  If you click the *Request Limit Increase* link, the system will
  generate a ticket with details of your current limits filled in. 
  Making a change requires describing the change you want and 
  submitting the ticket for processing. Update the ticket to 
  describe the change you want; then click *Submit Ticket*. 
 
  .. figure:: /_images/CreateTicketServersResourceLimit.png
     :scale: 80%
     :alt: In the generated ticket, 
         fill in the details you want to change. 
         
     In the generated ticket, 
     fill in the details you want to change.
 
The Cloud Control Panel may be the only interface you need to use,
especially if you don't need to heavily automate the management of your
cloud resources.

.. note::
   Under unusual circumstances,
   high-priority messages may be displayed in a banner 
   at the top of your Cloud Control Panel pages. 
   If you see such a message, 
   follow its instructions as soon as you can. 


Contents:

.. toctree::
   :maxdepth: 2

   setup_GUI
   cloudservers_GUI
   cloudnetworks_GUI
   cloudimages_GUI
   cloudblockstorage_GUI
   moreinfo_GUI
