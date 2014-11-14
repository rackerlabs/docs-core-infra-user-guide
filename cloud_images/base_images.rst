Base Images
===========

Images Lifecycle
----------------
To provide the best experience for our customers, 
we carefully
maintain the list of images displayed 
when building a new cloud server. 
This means that older versions 
of an operating system may sometimes be removed 
from the default list, 
usually shortly after a newer version is released. 
Images that have been published are never deleted, 
so even if they're removed
from the default list they will still be buildable 
via image ID using the Cloud
Servers API. 
Older images that have been removed 
from the default list 
are no longer maintained
and may not contain the most recent patches or package updates.

Patching
--------
Software patches are applied to base images as 
appropriate to each operating system: 

* Windows images are usually updated once per month,  
  consistently with Microsoft's patch release cycle.
* Linux images are updated on an as-needed basis which varies 
  from distribution to distribution.
   
Regardless of OS, critical patches are 
applied as soon as possible 
even if the change falls outside of our usual update
schedule.

..
   TODO
   Release Notes
   (This needs to be filled in 
   once public-facing release notes are available)

Default Configuration
---------------------
For Managed Infrastructure accounts, 
we keep the base configuration as close as
we can to distribution defaults. 
Some changes are necessary in order
for us to properly support the operating system in our environment. 
We try to
keep these changes to a minimum so users 
know exactly what behavior to expect.

For Managed Operations accounts, 
post-build automation runs to configure the operating system 
according to Rackspace best practices. 

For RackConnect accounts, 
default networking configurations are changed as needed.

..
   TODO
   For more information, check out

    * Cloud-Init (link to cloud-init docs once written)
    * Rackspace Nova Agent (link to agent docs once written)
