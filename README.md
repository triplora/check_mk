# check_mk
Plugins for Check_MK

xen - plugin

# local agent part for checking xen hosts
this is the version for xen releases that don't have --state.

todos:
check daemons -> inventory
grab performance data from xentop and turn it into perfdata
grab tmem & balloon statistics ( will need OVM3 beta to test)
check against /proc/xen/balloon - WARNING if dom0 balloon is enabled
if xend is not working, we'll go to critical regardless of other checks.
technically nothing needs xend - except that without it you can't migrate vm's
off a broken host. so this is something we wanna know about.

xen.vms - man

The  check matches the  list of running  virtual machines against  the list of 
 virtual  machines on the host. It will return "OK" if a VM is running, CRIT if 
 a  VM is in the states "c- crashed" or  "s - shutdown" or UNKWOWN if the VM is 
 not  found in the xm  list output. The check  supports only the old-style "xm" 
 command  set, support for "xl" as used in  Xen4.2 and up will be added. Citrix 
 XenServer will not be supported.
 
 xem.mem - man
 
 The  check queries the memory  under hypervisor control on  Xen hosts and will 
 display  the amounts used by dom0, used in  total, and the total memory of the 
 host.
 
