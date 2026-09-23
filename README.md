# wireshark-packet-analysis-lab
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
- Destination IP: `142.251.116.138`
- Protocol: ICMP
- Traffic observed: Echo Request and Echo Reply
- Result: Successful communication between the local host and remote server

## DNS Analysis
Coming soon.

## TCP Analysis
Coming soon.

## HTTPS/TLS Analysis
Coming soon.

## What I Learned
This lab helped me better understand how network protocols operate at the packet level and how Wireshark can be used to inspect, filter, and analyze network traffic.
