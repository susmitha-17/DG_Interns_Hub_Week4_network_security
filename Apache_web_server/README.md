Apache Web Server – Installation, Configuration and Network Accessibility Testing

This folder contains the practical evidence and screenshots related to the installation, configuration, execution, and testing of an Apache Web Server as part of Week 4 of the Cybersecurity Internship.

The objective of this activity was to configure a web server on the Ubuntu Linux target machine and verify that the service was accessible from the Kali Linux testing machine within an authorized virtual lab environment. This activity provided practical exposure to web server deployment, Linux service management, client-server communication, and basic network service verification.

Lab Environment:

- Attacker/Testing Machine: Kali Linux
- Target Machine: Ubuntu Linux
- Web Server: Apache2
- Network Type: VirtualBox Host-Only Network
- Lab Network: 192.168.56.0/24
- Kali Linux IP Address: 192.168.56.102
- Ubuntu Target IP Address: 192.168.56.101
- Apache HTTP Port: TCP 80

Apache Web Server Installation:

Apache2 was installed on the Ubuntu target machine using the Ubuntu package management system. After installation, the Apache service was started and configured to run as an active system service.

The following commands were used during the setup:

    sudo apt update
    sudo apt install apache2 -y
    sudo systemctl enable --now apache2

The Apache service status was then verified to ensure that the web server was running correctly.

Apache Service Verification:

The Apache service was checked using the Linux system service management command. The service was confirmed to be active and running on the Ubuntu target machine.

The Apache web server listens for HTTP requests on TCP port 80 by default. This port was later identified during the Nmap network scanning phase of the assessment.

Web Server Accessibility Testing:

After configuring Apache, connectivity to the web server was tested from the Kali Linux machine.

The following command was used:

    curl http://192.168.56.101

The successful response from the Apache web server confirmed that the Kali Linux testing machine could communicate with the Ubuntu target machine and access the HTTP service over the Host-Only lab network.

This test demonstrated a basic client-server interaction:

    Kali Linux
    192.168.56.102
          |
          | HTTP Request
          | TCP Port 80
          ↓
    Ubuntu Linux
    192.168.56.101
          |
          ↓
    Apache Web Server

Security and Networking Context:

Deploying an Apache web server provided a controlled service that could be monitored and assessed during the subsequent network security testing activities.

The HTTP service running on TCP port 80 was intentionally configured as part of the authorized cybersecurity lab. Its availability allowed the following activities to be performed:

- Network service discovery using Nmap.
- Service and version detection using Nmap.
- HTTP traffic generation for Wireshark analysis.
- Client-server communication testing.
- Packet-level observation of HTTP communication.
- Understanding how exposed network services can be identified during a security assessment.

The open HTTP port should not by itself be considered a vulnerability. It represents an intentionally enabled service required for the lab exercise. In a real-world environment, unnecessary services should be disabled and required services should be properly secured and monitored.

Evidence Included in This Folder:

1. `Task2_Apache_Running.png`

   This screenshot provides evidence that the Apache2 web server was successfully installed and running on the Ubuntu target machine. It demonstrates the service status and confirms that Apache was operational.

2. `Task2_Apache_From_Kali.png`

   This screenshot provides evidence that the Apache web server was successfully accessed from the Kali Linux testing machine using the target's Host-Only network IP address.

Purpose of the Activity:

The Apache setup was an important part of the Week 4 cybersecurity assessment because it created a real network service within the isolated virtual lab. This service was subsequently used for network scanning and traffic analysis.

The complete workflow was:

    Network Configuration
            ↓
    Ubuntu Target Setup
            ↓
    Apache2 Installation
            ↓
    Apache Service Verification
            ↓
    HTTP Connectivity Testing
            ↓
    Nmap Service Discovery
            ↓
    Wireshark HTTP Traffic Analysis

Key Learning Outcomes:

- Understanding the role of a web server in a network environment.
- Installing and configuring Apache2 on Ubuntu Linux.
- Managing Linux services using systemctl.
- Understanding HTTP communication and TCP port 80.
- Testing network connectivity between virtual machines.
- Using curl to verify web server accessibility.
- Understanding client-server communication.
- Preparing a controlled service for security assessment.
- Understanding how network services can be discovered using Nmap.
- Generating HTTP traffic for packet-level analysis using Wireshark.
- Developing practical Linux system administration and cybersecurity skills.

Security Considerations:

In a production environment, an Apache web server should be securely configured and regularly monitored. Important security practices include:

- Keep Apache and the underlying operating system updated.
- Disable unnecessary modules and services.
- Use HTTPS/TLS instead of unencrypted HTTP where appropriate.
- Restrict network access using firewall rules.
- Apply secure file and directory permissions.
- Avoid exposing unnecessary information through server configuration.
- Monitor web server logs for suspicious activity.
- Regularly perform vulnerability and configuration assessments.
- Use appropriate security headers and hardened configurations.

All Apache installation, configuration, connectivity testing, and security assessment activities documented in this folder were performed in a controlled and authorized virtual lab environment for educational and cybersecurity training purposes.
