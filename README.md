# netplan
 netplan - YAML network configuration abstraction for various backends

To solve the errors of netplan we refer to the error lines below:
After using this YAML file we will encounter the below warning after applying in netplan:

root@srv01:~# netplan apply
WARNING:root: Cannot call Open vSwitch: ovsdb-server.service is not running.

To solve the above Warning you have to install the below service:
********************************
root@srv1# apt-get install openvswitch-switch-dpdk

Then you can reapply the netplan
*******************************
root@srv01:~# netplan apply
