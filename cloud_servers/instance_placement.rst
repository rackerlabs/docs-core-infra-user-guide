Instance Placement
==================
When a virtual server is built a request is sent to the API and then the API hands that request off to a Scheduler. It's the job of the Scheduler to find a physical host to place the requested virtual server on using a wide array of factors.

By default the Scheduler will not place virtual servers on the same host as other virtual servers belonging to the same account, however this is not a hard fail and in some circumstances they can end up on the same host. For this reason every virtual server has a *Host ID* that can be referenced against the other virtual servers on an account to determine if any occupy the same host. 

