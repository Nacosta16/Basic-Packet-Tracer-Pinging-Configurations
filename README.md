# Basic Packet Tracer Configs/Topologies

<h2> In Cisco Packet Tracer, help desk technicians should be familiar with several network topologies to troubleshoot and assist users effectively. Here are three key topologies they should know </h2>
  
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

    - Open Cisco Packet Tracer → Drag and drop a Switch (e.g., 2960) onto the workspace.

    - Add End Devices → Drag multiple PCs (e.g., PC0 to PC3).

    - Connect Devices: Use Copper Straight-Through Cables to connect each PC to the switch.

    - Configure IP Addresses:
Click on each PC → Go to Desktop → Open IP Configuration.
Assign unique IP addresses in the same subnet (e.g., 192.168.1.10, 192.168.1.11, etc.).

    - Test Connectivity:
Open the Command Prompt (CMD) on any PC and use the ping command to check connectivity with others.
Example: ping 192.168.1.11
