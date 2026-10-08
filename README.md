# Wireshark-Packet-Analysis-for-SOC-Analysts

## Overview

This repository documents hands-on network traffic analysis labs using **Wireshark**, with an emphasis on practical skills required for entry-level Security Operations Center (SOC) analysts.

The objective is to develop the ability to capture, inspect, filter, and interpret network packets; identify suspicious network behavior; and document investigation findings using a structured SOC methodology.

The repository progresses from fundamental packet analysis to a complete network security investigation involving PCAP evidence, indicators of compromise (IOCs), and incident reporting.

## Objectives

- Understand packet captures and network traffic analysis.
- Navigate the Wireshark interface and inspect packet details.
- Apply display filters to isolate relevant network activity.
- Analyze TCP connections, handshakes, flags, and retransmissions.
- Investigate DNS queries and responses.
- Examine HTTP requests, responses, and headers.
- Analyze TLS/HTTPS traffic and available connection metadata.
- Identify ICMP activity and potential network reconnaissance.
- Recognize suspicious network communication patterns.
- Extract network indicators of compromise.
- Document findings in professional SOC investigation reports.

## Skills Demonstrated

**Network Traffic Analysis**
- Packet capture and PCAP examination
- TCP/IP protocol analysis
- Source and destination IP identification
- Port and protocol identification
- Packet filtering and traffic isolation

**Protocol Investigation**
- TCP handshake and flag analysis
- DNS query and response investigation
- HTTP request and response analysis
- TLS handshake and encrypted traffic metadata analysis
- ICMP traffic inspection

**SOC Investigation**
- Suspicious network activity identification
- Network connection correlation
- IOC extraction and documentation
- Network event timeline reconstruction
- Evidence-based alert investigation
- MITRE ATT&CK mapping where applicable
- Incident documentation and reporting

## Lab Environment

| Component | Environment |
|---|---|
| Host Operating System | Windows |
| Virtualization | Oracle VirtualBox |
| Analyst VM | Ubuntu 24.04 LTS |
| Packet Analysis Tool | Wireshark |
| Command-Line Tools | tcpdump, tshark, curl, ping, dig |
| Traffic Sources | Controlled lab traffic and training PCAP files |
| Documentation | GitHub Markdown and screenshots |

All packet captures and investigations are performed using authorized lab traffic, locally generated traffic, or publicly available training datasets.

## Tools & Technologies

- **Wireshark:** Packet capture and graphical traffic analysis.
- **TShark:** Command-line packet inspection and filtering.
- **tcpdump:** Network packet capture.
- **Linux/Bash:** Network diagnostics and traffic generation.
- **Curl:** HTTP/HTTPS traffic generation.
- **Dig:** DNS query generation and troubleshooting.
- **MITRE ATT&CK:** Security behavior classification where supported by investigation evidence.

## Labs & Projects

| # | Lab / Project | Focus |
|---|---|---|
| 01 | Wireshark Fundamentals | Interface navigation, packet capture, protocol identification |
| 02 | Wireshark Display Filters | Filtering by IP, port, protocol, and packet attributes |
| 03 | TCP Traffic Analysis | Three-way handshake, TCP flags, streams, retransmissions |
| 04 | DNS Traffic Analysis | Queries, responses, domains, DNS errors |
| 05 | HTTP & Web Traffic Analysis | HTTP methods, headers, status codes, web activity |
| 06 | TLS/HTTPS Traffic Analysis | TLS handshake, certificates, visible metadata |
| 07 | ICMP & Network Reconnaissance Analysis | ICMP activity, connectivity tests, scanning indicators |
| 08 | Suspicious Network Traffic Investigation | PCAP triage, suspicious communications, IOC extraction |
| Project | Network Security Incident Investigation | End-to-end PCAP investigation and professional incident report |

## Lab Methodology

Each lab follows a consistent workflow:

1. **Objective:** Define the network analysis skill being developed.
2. **Environment:** Identify the operating system, tools, and packet capture source.
3. **Tools Used:** Document relevant applications and commands.
4. **Steps Performed:** Capture or load traffic, apply filters, inspect packets, and analyze findings.
5. **SOC Relevance:** Explain how the activity relates to security monitoring and investigation.
6. **Evidence:** Include screenshots, filters, packet details, and supporting artifacts.
7. **Lessons Learned:** Summarize the technical findings and investigation skills developed.

## Core Wireshark Display Filters

| Filter | Purpose |
|---|---|
| `ip.addr == 192.168.1.10` | Traffic involving a specific IPv4 address |
| `ip.src == 192.168.1.10` | Traffic originating from an IPv4 address |
| `ip.dst == 192.168.1.20` | Traffic destined for an IPv4 address |
| `tcp` | Display TCP packets |
| `udp` | Display UDP packets |
| `dns` | Display DNS packets |
| `http` | Display recognized HTTP traffic |
| `icmp` | Display ICMP packets |
| `tcp.port == 443` | TCP traffic involving port 443 |
| `tcp.flags.syn == 1` | Packets with the TCP SYN flag set |
| `dns.flags.response == 0` | DNS queries |
| `dns.flags.response == 1` | DNS responses |
| `tcp.analysis.retransmission` | TCP packets identified as retransmissions |
| `ip.addr == 10.0.2.15 && tcp` | TCP traffic involving a specified IPv4 host |

These filters are used to narrow packet captures and isolate network activity relevant to an investigation.

## SOC Investigation Workflow

**1. Establish Context**

Identify the source of the PCAP, capture timeframe, relevant endpoints, and investigation objective.

**2. Identify Network Activity**

Review protocols, source and destination addresses, ports, packet counts, and communication patterns.

**3. Filter Relevant Traffic**

Apply Wireshark display filters to isolate suspicious hosts, protocols, conversations, or events.

**4. Analyze Evidence**

Inspect packet fields, DNS queries, TCP sessions, HTTP activity, TLS metadata, and observable network behavior.

**5. Extract Indicators**

Document relevant IP addresses, domains, URLs, ports, timestamps, and other supported network indicators.

**6. Determine Findings**

Distinguish confirmed observations from hypotheses. Evaluate whether the evidence supports benign, suspicious, or malicious activity.

**7. Document and Report**

Create a professional investigation report summarizing the evidence, findings, limitations, and recommended actions.

## Final Project — Network Security Incident Investigation

The final project integrates the skills developed throughout the eight labs into a complete PCAP-based investigation.

### Project Objectives

- Analyze an unfamiliar packet capture.
- Identify relevant hosts and network conversations.
- Investigate suspicious DNS, TCP, HTTP, and TLS activity.
- Reconstruct an evidence-supported activity timeline.
- Extract and document potential IOCs.
- Map observed behavior to MITRE ATT&CK where appropriate.
- Produce a professional SOC incident investigation report.

### Deliverables

- Investigation summary
- PCAP analysis methodology
- Network activity timeline
- Evidence screenshots
- IOC table
- Investigation findings
- MITRE ATT&CK mapping, if supported
- Recommended response actions
- Final incident report

## SOC Relevance

Packet analysis is a foundational skill for security monitoring, threat detection, and incident response.

SOC analysts use network traffic evidence to investigate suspicious connections, unusual DNS activity, potential command-and-control communications, reconnaissance, and other security events.

This repository demonstrates the ability to move beyond identifying ports and protocols toward interpreting network behavior, correlating evidence, and producing actionable investigation findings.

## Expected Outcomes

Upon completing this section, the portfolio will demonstrate practical familiarity with:

- Wireshark and packet capture analysis
- TCP/IP network behavior
- Network protocol investigation
- Suspicious traffic identification
- Network IOC extraction
- Evidence-based incident analysis
- Professional SOC reporting

The final investigation project serves as a portfolio artifact demonstrating an end-to-end network security analysis workflow.


**Portfolio Focus:** SOC Analyst Tier 1 | Blue Team | Network Security Monitoring | Incident Investigation
