# 🦈 Lab 08 Suspicious Network Traffic Investigation with Wireshark

## Objective
Investigate suspicious network activity using Wireshark by correlating multiple protocols, analyzing potential reconnaissance and web enumeration, identifying network indicators, and documenting findings in a SOC incident report.


## Skills Demonstrated
-Network traffic investigation

-Wireshark packet filtering and analysis

-TCP connection and flag analysis

-DNS query and response analysis

-HTTP request and response investigation

-ICMP reconnaissance analysis

-TLS handshake and encrypted traffic inspection

-Network timeline reconstruction

-Indicator of compromise extraction

-SOC alert triage and incident reporting

## Tools used
-Wireshark

-Ubuntu Linux

-Python 3

-curl

-ping

-Bash


## Steps performed
Generated a controlled packet capture containing normal and suspicious-looking activity.

Established a baseline of expected network traffic.

Investigated TCP connection attempts across multiple ports.

Analyzed repeated HTTP requests to sensitive paths.

Correlated source and destination addresses, ports, timestamps, and protocol behavior.

Extracted relevant network indicators.

Reconstructed a chronological timeline of observed activity.

Assessed whether the activity warranted escalation.

Documented findings and limitations in a SOC incident report.



## evidence (screenshots)



## SOC relevance 
SOC analysts frequently investigate alerts containing incomplete or ambiguous network evidence.

Packet analysis helps identify communication patterns, distinguish expected activity from anomalies, reconstruct timelines, and determine whether additional endpoint or server telemetry is needed.
