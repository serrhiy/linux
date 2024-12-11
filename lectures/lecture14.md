
1. ```ip``` - ip  -  show  / manipulate routing, network devices, interfaces and tunnels:
  a. ```ip address``` - display interfaces info;
  b. ```ip link set [down, up] <interface>``` - onn or off network interface;
  c. ```ip address [add, del] <network> dev <interface>``` - add/delete network address to interface;
  d. ```ip link set mtu <mtu> dev <interface>``` set mtu;
  e. ```ip link set address <mac address> dev <interface>``` set mac address;
  f. ```ip route show``` - display rout table;
  п. ```ip route add <network> via <network>``` - add network to rout table;
2. ```ifconfig``` - configure a network interface(old version ip);
3. ```nmtui``` - utilit for editing interfaces;
4. ```nmcli``` - command-line tool for controlling NetworkManager:
  a. ```nmcli connection show``` - display status connection;
  b. ```nmcli device status``` - display devices status;
  c. ```nmcli device status``` - display devices status;
  d. ```nmcli connection edit <interface>``` - edit connection(interactive);
  e. ```nmcli connection modify <interface> ipv4.addresses <address>``` - edit connection(need to restart enterface);
  f. ```nmcli connection [up,down] <interface>```;
  d. ```nmcli device show <interface>``` - display info about interface;
5. ```arp``` - manipulate the system ARP cache:
  a. ```arp -an``` - display arp table;
  b. ```arp -d``` - delete node;
  b. ```arp -s <network> <max address>``` - set node;