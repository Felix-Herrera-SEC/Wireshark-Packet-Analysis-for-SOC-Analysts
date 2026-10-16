# 🦈 Lab 07 ICMP & Network Reconnaissance Analysis with Wireshark

## Objective
Capture and analyze ICMP traffic using Wireshark to investigate echo requests and replies, ICMP error messages, TTL behavior, and network reconnaissance indicators.


## Skills Demonstrated
ICMP packet capture and protocol analysis

Echo request and echo reply identification

ICMP type and code interpretation

Source and destination IP analysis

ICMP sequence number and identifier inspection

Round-trip time analysis

TTL and traceroute investigation

Network reconnaissance pattern recognition

Wireshark display filtering

SOC alert triage and documentation



## Tools used
Wireshark

Ubuntu Linux

ping

traceroute

Python 3

Bash



## Steps performed
Captured ICMP echo request and reply packets.

Analyzed ICMP packet fields, including type, code, identifier, and sequence number.

Measured ICMP response timing.

Investigated ICMP error messages.

Analyzed TTL behavior and traceroute traffic.

Generated controlled repeated ICMP requests.

Used Wireshark filters to isolate ICMP patterns.

Documented a simulated network reconnaissance investigation.


## evidence (screenshots)



## SOC relevance 
ICMP analysis helps SOC analysts investigate network discovery, host reachability checks, reconnaissance, connectivity failures, and potentially suspicious repeated probing.

ICMP activity alone does not establish malicious intent. Analysts must consider frequency, targets, source context, and supporting security telemetry.
