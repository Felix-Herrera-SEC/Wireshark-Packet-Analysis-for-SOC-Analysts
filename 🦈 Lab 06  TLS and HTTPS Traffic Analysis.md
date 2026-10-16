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
1) <img width="765" height="207" alt="image" src="https://github.com/user-attachments/assets/04b05b7c-a58b-4fec-b69e-17183ada216b" />

2)<img width="770" height="301" alt="image" src="https://github.com/user-attachments/assets/847f96c4-b41e-41ae-83cf-ebf8d5167d33" />

3)<img width="882" height="182" alt="image" src="https://github.com/user-attachments/assets/d9f4d10a-0f1d-4d4b-ba68-c2e491f37b01" />

4)<img width="875" height="727" alt="image" src="https://github.com/user-attachments/assets/e0a86586-034c-4ac4-bdbf-0d9486b5c3ab" />

5)<img width="867" height="712" alt="image" src="https://github.com/user-attachments/assets/556b645b-1b26-403f-bd81-d8cc339122a7" />

6)<img width="867" height="732" alt="image" src="https://github.com/user-attachments/assets/07c352c9-86d4-4d67-b534-f1a6e5226826" />










## SOC relevance 
TLS analysis helps SOC analysts investigate encrypted network connections without requiring access to decrypted application content.

Analysts can use destination IP addresses, ports, handshake metadata, visible server names, certificate details, and connection patterns to support investigations involving suspicious external communication and potential command-and-control activity.
