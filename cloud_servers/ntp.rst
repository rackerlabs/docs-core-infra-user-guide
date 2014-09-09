NTP
===
During boot Linux sets the system clock to the same time as the physical 
server's hardware clock. At this point Linux maintains the clock separately
from the hardware clock. If the hardware clock is incorrect then this can 
cause issues with anything that relies on having the correct time.

NTP or network time protocol is an open source Linux package that allows a
server to sync it's system clock with a pool of authoritative NTP servers.
http://www.ntp.org maintains a list of public NTP servers to sync
from.

Rackspace maintains internal NTP servers in each region that can be used to sync
with.

====== ========================          ===============
Region Hostname                          Timezone
====== ========================          ===============
DFW    time.dfw1.rackspace.com           CST (UTC-06:00) 
DFW    time2.dfw1.rackspace.com          CST (UTC-06:00)
ORD    time.ord1.rackspace.com           CST (UTC-06:00)
ORD    time2.ord1.rackspace.com          CST (UTC-06:00)
IAD    time.iad1.rackspace.com           CST (UTC-06:00)
IAD    time2.iad1.rackspace.com          CST (UTC-06:00)
LON    time.lon1.rackspace.com           GMT (UTC+00:00)
LON    time2.lon1.rackspace.com          GMT (UTC+00:00)
HKG    time.hkg1.rackspace.com           HKT (UTC+08:00)
HKG    time2.hkg1.rackspace.com          HKT (UTC+08:00)
SYD    time.syd1.rackspace.com           AET (UTC+10:00)
SYD    time2.syd1.rackspace.com          AET (UTC+10:00)
====== ========================          =============== 