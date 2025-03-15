# Basic Packet Tracer Configs/Topologies

<h2> Learning with Cisco Packet Tracer, help desk technicians have the ability to be familiar with several network topologies to troubleshoot and assist users effectively. Here are three key topologies they should know </h2>
  
- <b> Star Topology </b>

  - All devices connect to a central switch or hub. If one device fails, it doesn’t impact the rest of the network.
  - Why it’s Important: Most modern LANs use this topology. Help desk technicians should understand switch configurations, VLANs, and common connection issues.

- <b> Mesh Topology (Full or Partial) </b>

  - Devices are interconnected, providing multiple paths for data transmission. This is common in WANs and enterprise networks.
  - Why it’s Important: Mesh networks improve redundancy and reliability. A help desk must understand routing, link redundancy, and troubleshooting path failures.

- <b> Bus or Ring Topology </b>

  - Older, also known as legacy, networks used bus (single backbone cable) and ring (devices connected in a loop). Some hybrid networks may still use these structures.
  - Why it’s Important: Though less common today, legacy systems still exist. Understanding troubleshooting methods for shared bandwidth and token-passing networks is useful.
 
<H2> How to configure these topologies in packet tracer </H2>

 -  <h3> Star Topology </h3>

 Open Cisco Packet Tracer and drop a switch, located in the bottom left corner, onto the workspace.

<img src="https://sigmawire.net/i/03/vz3NqG.png" height="35%" width="35%" alt="VirtualBox set up wizard" />

 Add End Devices, any 2 PC's will be fine

Connect Devices using a copper straight through cable to connect each PC to the switch (You can also select the auto icon below to automatically connect the correct cable)

<img src="https://sigmawire.net/i/03/FpVB0T.png" height="35%" width="35%" alt="VirtualBox set up wizard" />

   - Configure IP Addresses: Click on each PC, go to Desktop, then IP Configuration. Assign unique IP addresses in the same subnet. For a example, PC 2 will have 192.168.1.10 abd PC 0 
 will have 192.168.1.11. They are different IP's but still on the same subnet of 255.255.255.0

<img src="https://sigmawire.net/i/03/U9NZB0.png" height="35%" width="35%" alt="VirtualBox set up wizard"/>

<img src="https://sigmawire.net/i/03/tTi3wI.png" height="35%" width="35%" alt="VirtualBox set up wizard"/>

<img src="https://sigmawire.net/i/03/l3WDoy.png" height="35%" width="35%" alt="VirtualBox set up wizard"/>

   - Test Connectivity:

Open the Command Prompt (CMD) on any PC and use the ping command to check connectivity with others to ensure the topology is connected properly

<img src="https://sigmawire.net/i/03/kfRUzo.png" height="35%" width="35%" alt="VirtualBox set up wizard"/>

<img src="https://sigmawire.net/i/03/l1LXEP.png" height="35%" width="35%" alt="VirtualBox set up wizard"/>


-  As you can see, when you ping the PC configured to your network, it goes through, otherwuse it will come back as "request timed out"
  

- <h3> Mesh Topology </h3>

    - Drag & Drop Multiple Routers (e.g., Router0, Router1, Router2)

   - Add End Devices: Connect a PC or Server to each router using Switches

   - Connect the Routers: Use Serial Cables (DCE to DTE) or Ethernet Cables for inter-router communication

   - Assign IP Addresses to Routers: Go to Router CLI → Use the following commands to set up interfaces:
bash
Copy
Edit
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown
Repeat this for all routers with different subnets.

   - Enable Routing (Use RIP, OSPF, or EIGRP): bash Copy Edit
Router(config)# router ospf 1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0

   - Test with Ping: Ensure all devices can communicate across different paths

- <h3> Bus/Legacy Topology </h3>

   - Drag & Drop a Hub (instead of a switch)

   - Connect Multiple PCs using Straight-Through Cables

   - Assign IP Addresses (same as in Star Topology)

   - Test with Ping

