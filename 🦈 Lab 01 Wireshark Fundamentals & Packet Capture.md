# 🦈 Lab 01 — Wireshark Fundamentals & Packet Capture

## Objective
Capture and analyze network traffic using Wireshark in an Ubuntu Linux environment. Identify source and destination IP addresses, protocols, TCP/UDP ports, timestamps, and packet-level information relevant to SOC monitoring and incident investigation.


## Skills Demonstrated
-Network packet capture and PCAP analysis

-Wireshark interface navigation

-TCP/IP packet inspection

-Source and destination IP identification

-TCP/UDP port identification

-ICMP traffic analysis

-DNS query and response analysis

-Basic Wireshark display filtering

-Network evidence collection and documentation



## Tools used
Wireshark

Ubuntu Linux

Bash

ping

dig

curl

ip



## Steps performed
1)Installed and configured Wireshark.

2)Identified the active network interface.

3)Captured live network traffic.

4)Generated controlled ICMP, DNS, and HTTPS traffic.

5)Examined packet list, details, and bytes.

6)Identified packet addresses, ports, and protocols.

7)Applied basic display filters.

8)Saved a PCAPNG file for further analysis.


## evidence (screenshots)

1)Installed wireshark using the apt install wireshark command and configured Wireshark by checkng my main interface using the ip a command on the terminal and opened it

<img width="741" height="412" alt="image" src="https://github.com/user-attachments/assets/9ee6bb5e-cf0d-4a60-9e17-df1c0ce11c34" />

<img width="767" height="160" alt="image" src="https://github.com/user-attachments/assets/6e7ceac5-f26e-4aab-89f5-837a2409eee3" />

2)Wireshark interface navigation, used the ping, dig and curl commands to generate ICMP, DNS and Https traffic.

then used the red square stop button inside wireshark to stop the capture.

<img width="1221" height="586" alt="image" src="https://github.com/user-attachments/assets/7ae6818c-33b7-4553-bfaf-57eb9ba81764" />

3) Filterd by ICMP in the wireshark filter bar and then ran another ping using the ping command.

<img width="1162" height="855" alt="image" src="https://github.com/user-attachments/assets/b6f274f1-2843-426d-a5cf-412178377021" />

Here I was able to identify the source IP: 1.1.1.1, the destination IP: 10.0.2.15 the type of of ICMP: Echo, and code: 0, and the sequence number: 1/256

4) then I filtered for DNS and ran traffic through the dig youtube.com command.

<img width="750" height="555" alt="image" src="https://github.com/user-attachments/assets/f2bdef96-bf71-4282-98dd-b2c0e70231eb" />

and I was able to identify: 

What domain was queried? youtube.com


Which DNS server received the query?  10.0.0.1


What type of DNS record was requested? stdard query


What IP addresses were returned? 

<img width="555" height="102" alt="image" src="https://github.com/user-attachments/assets/9946b60b-5304-42c9-8916-501384ff86c0" />

Was the response successful? No error

## SOC relevance 

SOC analysts use packet captures to investigate network connections, validate alerts, analyze protocol behavior, identify communicating endpoints, and collect evidence during incident investigations.


