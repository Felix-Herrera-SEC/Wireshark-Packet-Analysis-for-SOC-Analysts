# 🦈 Lab 05 HTTP & Web Traffic Analysis with Wireshark

## Objective
Capture and analyze HTTP traffic using Wireshark to investigate web requests, server responses, HTTP methods, headers, URLs, status codes, and suspicious web activity relevant to SOC operations.


## Skills Demonstrated
HTTP packet capture and analysis

Wireshark display filtering

HTTP GET and POST request identification

HTTP header inspection

HTTP status code interpretation

HTTP request and response correlation

TCP stream reconstruction

Web traffic timeline analysis

Suspicious URL and request investigation

Network indicator extraction

SOC incident documentation

## Tools used
Wireshark

Ubuntu Linux

Python 3

curl

Bash

## Steps performed
Started a controlled HTTP web server.

Captured HTTP traffic over the loopback interface.

Identified HTTP GET requests and server responses.

Inspected HTTP request headers and URLs.

Generated and analyzed POST requests.

Investigated HTTP status codes.

Reconstructed an HTTP conversation using Follow TCP Stream.

Analyzed simulated suspicious web traffic.

Documented findings and supporting evidence.


## evidence (screenshots)

1)<img width="696" height="442" alt="image" src="https://github.com/user-attachments/assets/fd24f0e4-4685-48dc-9807-eceb3a1d27e3" />

2)<img width="877" height="91" alt="image" src="https://github.com/user-attachments/assets/b7c6ee8b-50fe-4ae0-b17b-0b2e1263cf3e" />

3)<img width="432" height="436" alt="image" src="https://github.com/user-attachments/assets/032b1bf2-8358-4d65-bbc5-0de7d4f01849" />

4)<img width="467" height="377" alt="image" src="https://github.com/user-attachments/assets/c4810719-7019-4c61-982c-e4e6e3a527a7" />

5)<img width="582" height="386" alt="image" src="https://github.com/user-attachments/assets/c1353505-5459-4a79-8da3-a2b4f40dafe4" />

## SOC relevance 
HTTP traffic analysis helps SOC analysts investigate suspicious web requests, unauthorized resource access, unusual user agents, web scanning behavior, and possible malicious downloads.

HTTP metadata and request patterns can provide evidence of suspicious behavior, but conclusions require supporting context.



