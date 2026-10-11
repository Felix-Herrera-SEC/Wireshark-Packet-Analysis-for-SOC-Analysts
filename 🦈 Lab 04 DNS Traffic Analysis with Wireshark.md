# 🦈 Lab 04 — DNS Traffic Analysis with Wireshark

## Objective
Capture and analyze DNS traffic using Wireshark to investigate domain resolution, DNS record types, failed queries, and network activity patterns relevant to SOC monitoring.


## Skills Demonstrated
DNS packet capture and protocol analysis

Wireshark display filtering

DNS query and response correlation

DNS transaction ID analysis

A, AAAA, MX, TXT, CNAME, and NS record identification

NXDOMAIN and DNS error analysis

Repeated DNS query analysis

Suspicious domain activity investigation

Network indicator extraction

SOC investigation documentation


## Tools used
Wireshark

Ubuntu Linux

dig

Bash

resolvectl



## Steps performed
Identified the DNS resolver used by the Ubuntu VM.

Captured DNS queries and responses.

Analyzed DNS packet fields and transaction IDs.

Investigated common DNS record types.

Generated and analyzed NXDOMAIN responses.

Examined repeated DNS queries and timing.

Extracted DNS indicators from packet captures.

Completed a simulated suspicious DNS activity investigation.


## evidence (screenshots)
1) Used resolvectl status command to verify DNS resolver IP, then generated DNS queries using the dig @1.1.1.1 google.com A command, then opened wireshark filtered for DNS traffic to see the query packets.

<img width="950" height="216" alt="image" src="https://github.com/user-attachments/assets/8236c063-1dda-416a-ad6f-1a7101e6831c" />

I was able to identify the following information:

Source IP address: 10.0.2.15

Destination IP address: 1.1.1.1

DNS query name: google.com

Query type: standarnd

Packet timestamp: 3.63

2) Used the dns.flags.response == 0 to filter for all DNS queries.

<img width="951" height="201" alt="image" src="https://github.com/user-attachments/assets/ab046a94-caaa-4a68-93e4-32673ce033c4" />

Then used the dns.flags.response == 1 filter to filter for the responses only.

<img width="955" height="241" alt="image" src="https://github.com/user-attachments/assets/e4077d2b-6427-47e9-9e4b-7ed7d8d76ba5" />

Then used the dns.qry.name == "google.com" command to filter for a specific domain name.

<img width="955" height="211" alt="image" src="https://github.com/user-attachments/assets/724ae673-070a-44c4-945c-e7f96e5e3b74" />

Then opened the DNS query section inside ubuntu and was able to get the following information:

<img width="465" height="302" alt="image" src="https://github.com/user-attachments/assets/17e8967d-1612-410a-b7bc-737ac21c6145" />

Transaction IDs: 0xae11

Flags: 0x0120 Standard Query

Questions: 1

Queries: google.com: type A, Class IN

Answers: 0



## SOC relevance 
DNS analysis helps SOC analysts investigate domains queried by endpoints, identify unusual resolution patterns, correlate network indicators, and support investigations involving phishing, malware, and possible command-and-control activity.

Suspicious DNS patterns require validation using additional network and endpoint evidence.



