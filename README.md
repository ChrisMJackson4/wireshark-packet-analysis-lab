# Wireshark Packet Analysis Lab

## Objective
The purpose of this lab was to capture and analyze common network traffic using Wireshark. I used packet captures to examine how protocols such as ICMP, DNS, TCP, and HTTPS/TLS communicate across a network.

## Tools Used
- Wireshark
- Windows 11
- Command Prompt / PowerShell
- Google Chrome

## Protocols Analyzed
- ICMP
- DNS
- TCP
- HTTPS/TLS

## ICMP Analysis
I used the `ping` command to generate ICMP traffic and captured the packets in Wireshark.

The capture showed ICMP Echo Requests sent from my local device to a Google server, followed by ICMP Echo Replies from the server.

This demonstrated how ICMP can be used to test network connectivity and verify that a remote host is reachable.

### ICMP Findings
- Source IP: `10.152.23.157`
- Destination IP: `8.8.8.8`
- Protocol: ICMP
- Traffic observed: Echo Request and Echo Reply
- Result: Successful communication between the local host and remote server

### ICMP Ping Request and Reply

The screenshot below shows ICMP Echo Request and Echo Reply packets between my computer and Google's DNS server at `8.8.8.8`.

This demonstrates how ICMP can be used to test whether a remote host is reachable and responding over the network.

<img width="1252" height="808" alt="Screenshot 2026-09-23 172634" src="https://github.com/user-attachments/assets/1ef89694-371f-40ec-9892-01c3d11a7478" />

## DNS Analysis

Using the `dns` display filter in Wireshark, I observed DNS queries and responses generated while accessing websites.
DNS is responsible for translating human-readable domain names, such as `google.com`, into IP addresses that computers use to communicate across networks.
The capture showed my system sending a DNS query requesting the IP address associated with a domain name and receiving a response containing the resolved IP address.
This demonstrated how DNS resolution occurs before a device establishes a connection with a remote server.

### DNS Query and Response

The screenshot below shows my computer sending a DNS query for `dns.google` to Google's DNS server at `8.8.8.8`.

Wireshark captured the DNS response returning an IPv4 address for the domain, demonstrating how DNS translates human-readable domain names into IP addresses used for network communication.
<img width="1233" height="733" alt="image" src="https://github.com/user-attachments/assets/b2d426d0-b6e6-4c42-97b4-961637f2c435" />

## TCP Analysis
Using the `tcp` display filter in Wireshark, I examined TCP connections between my computer and remote servers.
I identified the TCP three-way handshake used to establish a reliable connection:
1. SYN — The client requests a connection.
2. SYN-ACK — The server acknowledges the request and responds.
3. ACK — The client acknowledges the server, completing the connection.
I also observed TCP traffic using port 443, which is commonly used for HTTPS connections. After the TCP connection was established, encrypted TLS traffic was exchanged between the client and server.
This analysis demonstrated how TCP establishes reliable connections before application-layer communication occurs.

##### TCP Three-Way Handshake

The screenshot below shows a TCP connection being established using the three-way handshake. The client sends a SYN packet, the server responds with SYN-ACK, and the client completes the handshake with an ACK.

This connection was established over TCP port 443 before TLS-encrypted communication began.

<img width="1023" height="886" alt="Screenshot 2026-09-22 191205" src="https://github.com/user-attachments/assets/d137a4f9-a3db-4c5a-8483-84f5d4d85af4" />




## HTTPS/TLS Analysis
Using the `tls` display filter in Wireshark, I observed encrypted HTTPS traffic between my computer and remote web servers.
HTTPS uses TLS to encrypt data being transmitted between a client and server. Unlike unencrypted HTTP traffic, the actual contents of the communication cannot normally be read directly from the packet capture.
I observed TLS handshake traffic used to establish a secure connection before encrypted application data was exchanged.
I also observed HTTPS traffic using TCP port 443.
This demonstrated how TLS protects the confidentiality of network communications while Wireshark can still reveal information such as source and destination IP addresses, ports, packet sizes, and connection activity.
## HTTPS and TLS Screenshot
<img width="1081" height="637" alt="Screenshot 2026-09-23 170626" src="https://github.com/user-attachments/assets/327c67ad-3f6f-4323-aca7-c7c2a2a9b0e2" />
## What I Learned
This lab helped me understand how network protocols operate at the packet level and how Wireshark is used to inspect, filter, and analyze network traffic. I gained first hand experience identifying ICMP traffic, DNS resolution, TCP connection establishment, and TLS-encrypted communication.
