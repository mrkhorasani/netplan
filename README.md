# netplan
 netplan - YAML network configuration abstraction for various backends

To solve the errors of netplan we refer to the error lines below:
After using this YAML file we will encounter the below warning after applying in netplan:
![image](https://github.com/mrkhorasani/netplan/assets/51242725/849a1e27-f85f-4d56-b3a4-5ef47a451054)

root@srv01:~# netplan apply
WARNING:root: Cannot call Open vSwitch: ovsdb-server.service is not running.

********************************
To solve the above Warning you have to install the below service:
```
apt-get install openvswitch-switch-dpdk
```
*******************************
Then you can reapply the netplan
```
netplan apply
```
