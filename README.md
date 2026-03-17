# Security and High Availability – ASIR Module

This repository contains the practical assignments from the Security and High Availability module.  
The documentation is in Spanish and organized by topics to make navigation easier. If you need any clarification, I’ll be happy to help 😁. (The practices are documented through PDF files containing screenshots and explanations)

## Contents

### UT1 – Cryptography
Cryptographic mechanisms used to protect information in modern systems. It covers hashing algorithms, symmetric and asymmetric encryption, and the use of digital signatures to ensure integrity, confidentiality, and authenticity. The unit also includes a practical password‑auditing exercise using tools such as **John the Ripper**.

### UT2 – Active Security and Host Monitoring
The first practice involves performing vulnerability scanning with **Nessus**, identifying system weaknesses, evaluating risk levels, and interpreting security reports to understand potential attack vectors. The second practice introduces host‑based intrusion detection through the deployment of **Wazuh** as a centralized manager. In this setup, multiple agents forward their log data to the Wazuh server, enabling real‑time monitoring, log analysis, and threat detection across the network’s hosts.

### UT3 – Firewall (Iptables)
The practices explore different filtering scenarios, including controlling HTTP traffic, implementing NAT rules for address translation, managing ICMP requests, and applying connection‑tracking states such as NEW and ESTABLISHED to regulate session behavior. Also something interesting is the creation of a whitelist‑based security policy, allowing only explicitly authorized traffic while blocking all other network flows. 

### UT4 – VPN and Remote Access (This one is very interesting 👌)
Deployment of a VPN server using **WireGuard** and the configuration of remote access to cloud‑hosted infrastructure. The practice begins with the setup of a WireGuard server on an **AWS** EC2 instance, enabling IP forwarding, generating cryptographic keys, and defining the server‑side interface and firewall rules required for encrypted tunneling. The client configuration is performed from Windows, establishing a secure connection to the server using the instance’s public endpoint and validating the change in network routing once the VPN is active. The unit also covers remote administration of the EC2 instance via SSH and secure file transfer operations between the local machine and the cloud server, demonstrating how VPN connectivity and remote access protocols integrate to provide a protected management environment.

### UT5 – Proxy (This is also quite interesting 👌)
Introduces the use of proxy servers as a security and traffic‑management layer within a network, focusing on the deployment and configuration of **Squid** as a web proxy. The practice covers the essential components of Squid’s operation, including rule‑based access control, URL filtering, domain blocking, and authentication mechanisms for user‑based restrictions. Students learn how to regulate HTTP and HTTPS traffic, apply content‑filtering policies, and enforce organizational browsing rules through ACLs. The unit also explores advanced features such as connection limits, session timeouts, and the implementation of a transparent proxy using firewall redirection, enabling traffic interception without client‑side configuration.

### UT6 – High Availability (👌 too)
Deployment of a load‑balanced web architecture in AWS. The practice begins with the creation and configuration of multiple Ubuntu‑based web servers, each running Apache and serving distinct content. After preparing the initial instance, a machine image is generated to replicate the environment and launch an identical second server, ensuring consistency across the infrastructure. Both instances are then registered in a target group and placed behind an Elastic Load Balancer, which distributes incoming traffic across the servers to guarantee service continuity and improve fault tolerance. The final stage involves testing the setup by accessing the load balancer’s DNS endpoint and observing how requests alternate between the different backend servers.
