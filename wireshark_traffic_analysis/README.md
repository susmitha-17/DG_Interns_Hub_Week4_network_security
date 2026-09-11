Wireshark Traffic Analysis – Network Traffic Monitoring and Protocol Analysis

This folder contains the practical evidence and screenshots related to network traffic analysis performed using Wireshark as part of Week 4 of the Cybersecurity Internship.

The objective of this activity was to capture, monitor, and analyze different types of network traffic generated within an authorized virtual lab environment. Wireshark was used as a network protocol analyzer to observe packet-level communication and understand how different protocols operate across the network.

The traffic analysis covered the following protocols:

1. HTTP Traffic Analysis
   - HTTP traffic was generated between the Kali Linux attacker machine and the Ubuntu target machine running an Apache web server.
   - The HTTP communication was captured and analyzed using Wireshark.
   - The filter `tcp.port == 80` was used to isolate web traffic associated with the Apache HTTP service.
   - The captured packets helped demonstrate TCP-based communication between the client and web server.

2. ICMP Traffic Analysis
   - ICMP traffic was generated using ping communication between the Kali Linux and Ubuntu virtual machines.
   - The Wireshark filter `icmp` was used to identify and analyze ICMP Echo Request and Echo Reply packets.
   - This activity demonstrated how ICMP can be used to verify network connectivity and how ping traffic appears at the packet level.

3. DNS Traffic Analysis
   - DNS traffic was captured while performing a controlled DNS lookup using `nslookup`.
   - The Wireshark filter `dns` was used to identify DNS query and response packets.
   - The analysis demonstrated how domain-name resolution works and how DNS communication can be observed using a packet analyzer.
   - DNS testing was performed using temporary NAT connectivity in the controlled lab environment, while the main cybersecurity lab network remained configured using the VirtualBox Host-Only network.

The Wireshark analysis was performed in an authorized virtual lab environment consisting of Kali Linux and Ubuntu virtual machines. The lab network used the VirtualBox Host-Only network `192.168.56.0/24`, with Kali Linux configured as the testing/attacker machine (`192.168.56.102`) and Ubuntu configured as the target machine (`192.168.56.101`).

Files included in this folder:

- `Task4_HTTP_Traffic.png` – Wireshark evidence of HTTP traffic captured during communication with the Apache web server.
- `Task4_ICMP_Traffic.png` – Wireshark evidence of ICMP Echo Request and Echo Reply packets generated using ping.
- `Task4_DNS_Traffic.png` – Wireshark evidence of DNS query and response traffic generated using `nslookup`.

Key learning outcomes from this activity include:

- Understanding packet capture and network traffic monitoring.
- Identifying common network protocols using Wireshark.
- Applying Wireshark display filters to isolate specific traffic.
- Analyzing HTTP, ICMP, and DNS packets.
- Understanding client-server communication at the packet level.
- Observing network communication generated during security testing.
- Developing practical skills in network troubleshooting and security monitoring.
- Understanding how packet analysis can support network security investigations and SOC activities.

All activities documented in this folder were performed in a controlled and authorized virtual lab environment for educational and cybersecurity training purposes.
