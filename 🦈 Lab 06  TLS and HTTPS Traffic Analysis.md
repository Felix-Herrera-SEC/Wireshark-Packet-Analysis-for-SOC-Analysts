# 🦈 Lab 06  TLS and HTTPS Traffic Analysis

## Objective
Capture and investigate TLS/HTTPS network traffic using Wireshark to analyze encrypted connections, TLS handshakes, protocol versions, visible server names, certificate information, and network metadata relevant to SOC investigations.


## Skills Demonstrated
-TLS/HTTPS packet capture

-Wireshark display filtering

-TLS ClientHello and ServerHello analysis

-TLS version identification

-Server Name Indication (SNI) inspection

-TLS certificate analysis

-Encrypted application traffic identification

-Network connection metadata analysis

-Suspicious TLS activity triage

-SOC investigation documentation

## Tools used
-Wireshark

-Ubuntu Linux

-curl

-OpenSSL

-dig

-Bash



## Steps performed

-Configured the Ubuntu VM for HTTPS traffic analysis.

-Captured HTTPS connections using Wireshark.

-Identified TLS handshake packets.

-Inspected ClientHello and ServerHello messages.

-Identified TLS versions and negotiated cipher suites.

-Examined SNI and certificate information where visible.

-Analyzed encrypted application traffic.

-Extracted connection metadata for SOC investigation.


## evidence (screenshots)



## SOC relevance 
TLS analysis helps SOC analysts investigate encrypted network connections without requiring access to decrypted application content.

Analysts can use destination IP addresses, ports, handshake metadata, visible server names, certificate details, and connection patterns to support investigations involving suspicious external communication and potential command-and-control activity.
