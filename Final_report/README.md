Week 4 Final Report – Network Security Assessment

This folder contains the final documentation and report for Week 4 of the Cybersecurity Internship at DG Interns Hub.

The Week 4 assessment focused on establishing a controlled virtual network environment, configuring a web service, performing network reconnaissance, analyzing network traffic, and documenting the complete security assessment workflow.

The assessment was conducted in an authorized and isolated virtual lab environment using Kali Linux and Ubuntu Linux virtual machines connected through a VirtualBox Host-Only network.

Project Overview:

The primary objective of this assessment was to gain practical experience in basic network security testing and monitoring by combining network configuration, service deployment, network scanning, and packet-level traffic analysis.

The assessment followed the workflow:

    Network Setup
          ↓
    Apache Web Server Configuration
          ↓
    Nmap Network Scanning
          ↓
    Wireshark Traffic Analysis
          ↓
    Security Observations
          ↓
    Documentation & Final Assessment

Lab Environment:

- Attacker/Testing Machine: Kali Linux
- Target Machine: Ubuntu Linux
- Virtualization Platform: Oracle VirtualBox
- Network Type: VirtualBox Host-Only Network
- Lab Network: 192.168.56.0/24
- Kali Linux IP: 192.168.56.102
- Ubuntu Target IP: 192.168.56.101
- Web Server: Apache2
- HTTP Service: TCP Port 80

Assessment Tasks:

1. Basic Network Setup

The virtual lab network was configured using a VirtualBox Host-Only network. Kali Linux and Ubuntu were placed on the same isolated network to enable controlled communication between the testing and target machines.

Connectivity was verified using ICMP ping tests between the virtual machines.

2. Apache Web Server Configuration

Apache2 was installed and configured on the Ubuntu target machine.

The Apache service was verified to ensure that it was active and running. HTTP accessibility was then tested from Kali Linux using the target machine's IP address.

This provided a functional network service that could be used for subsequent scanning and traffic analysis activities.

3. Nmap Network Scanning

Nmap was used from Kali Linux to perform network service discovery against the Ubuntu target.

The assessment included:

- Basic host and port scanning.
- Identification of accessible TCP ports.
- Service and version detection using Nmap.
- Saving the scan output for documentation.

The scan identified the intentionally configured Apache HTTP service on TCP port 80.

The Nmap results were saved separately as:

    week4_nmap_scan.txt

4. Wireshark Traffic Analysis

Wireshark was used to capture and analyze network traffic generated during controlled testing activities.

Three major traffic types were analyzed:

- HTTP traffic
- ICMP traffic
- DNS traffic

The following Wireshark filters were used:

    tcp.port == 80
    icmp
    dns

HTTP traffic was generated through communication with the Apache web server.

ICMP traffic was generated using ping between the Kali Linux and Ubuntu machines.

DNS traffic was captured during a controlled DNS lookup using nslookup. DNS testing temporarily used NAT connectivity for Internet-based name resolution; the primary cybersecurity lab remained configured using the Host-Only network.

Security Observations:

The assessment demonstrated how an exposed network service can be identified through network scanning and subsequently monitored through packet analysis.

Key observations included:

- Successful communication between the Kali Linux and Ubuntu virtual machines.
- Apache HTTP service successfully deployed on the Ubuntu target.
- TCP port 80 identified as an accessible HTTP service.
- HTTP communication observed using Wireshark.
- ICMP Echo Request and Echo Reply traffic successfully captured.
- DNS queries and responses successfully captured.
- Nmap and Wireshark can complement each other during basic network security assessments.

The presence of an open HTTP port was not treated as a vulnerability by itself because Apache was intentionally deployed as part of the authorized lab exercise.

Tools and Technologies:

- Kali Linux
- Ubuntu Linux
- Oracle VirtualBox
- Apache2
- Nmap
- Wireshark
- curl
- ping
- nslookup

Evidence and Documentation:

The final report includes detailed explanations, screenshots, network configuration information, command outputs, traffic analysis evidence, security observations, and conclusions from each stage of the assessment.

Supporting evidence is organized across the Week 4 GitHub repository:

- 01-Lab-Setup
- 02-Apache-Web-Server
- 03-Nmap-Scanning
- 04-Wireshark-Traffic-Analysis
- 05-Final-Report
- 06-PPT

Files in this folder:

- Week-4-Network-Security-Report.pdf
- Week-4-Network-Security-Report.docx

Learning Outcomes:

Through this assessment, the following practical skills were developed:

- Basic virtual network configuration.
- Linux networking fundamentals.
- Apache web server deployment.
- Linux service management.
- Network connectivity testing.
- Nmap-based network reconnaissance.
- Service and version identification.
- Packet capture and protocol analysis using Wireshark.
- HTTP, ICMP, and DNS traffic analysis.
- Basic security observation and documentation.
- Understanding the relationship between network reconnaissance and traffic monitoring.
- Preparing professional cybersecurity assessment documentation.

Conclusion:

The Week 4 assessment provided practical exposure to the initial stages of a network security assessment. By combining virtual network configuration, web server deployment, Nmap scanning, and Wireshark traffic analysis, the exercise demonstrated how network services can be deployed, discovered, monitored, and documented in a controlled environment.

The activity strengthened practical knowledge of networking and cybersecurity tools while providing hands-on experience relevant to areas such as network security, SOC monitoring, security analysis, and incident investigation.

All activities documented in this report were performed in a controlled and authorized virtual lab environment for educational and cybersecurity training purposes.
