# Network setup Documentation
###Device list 

1. Router1
-Device Type: Router
-Device Module: ISR4331
-Assigned IP Address: 168.90.0.1/16
2. Switch1 
-Device Type: Switch
-Device Module: ISR4331
3. PC0
-Device Type: PC
-Device Module: PC-PT
-Assigned IP Address: 168.90.0.5
4. PC3
-Device Type: PC
-Device Module: PC-PT
-Assigned IP Address: 168.90.0.3
5. Server1
-Device Type: Server 
-Device Module: Server-PT
6. Laptop
-Device Type: Laptop
-Device Module: Laptop-PT
-Assigned IP Address: 168.90.0.2
7. Switch2 
-Device Type: Switch
-Device Module: 2960 IOS15
8. Server 
-Device Type: Server
-Device Module: Server-PT
-Assigned IP Address: 219.3.0.1/16
9. Server2
-Device Type: Server
-Device Module: Server-PT
-Assigned IP Address: 219.3.0.2/16
10. PC2
-Device Type: PC
-Device Module: PC-PT
-Assigned IP Address: 219.3.0.3/16
### New PCs Added: 
1. PC4 (connected to Switch1)
-IP Address: 168.90.0.6/16
2. PC5 (connected to Switch2)
-IP Address: 210.3.0.4/16
### DCHP Configuration Details: 
The following steps will configure DHCP on the router. 
Router# configure terminal 
Router(config)# ip dhcp pool LAN_POOL
Router(config-dhcp)# network 168.90.0.0 255.255.0.0
Router(config-dhcp)# default-router 168.90.0.0
Router(config-dhcp)# dns-server 8.8.8.8
Router(config)# ip dhcp excluded-address 255.255.0.0
Router(config)# ip dhcp-server
Router# show ip dhcp binding

