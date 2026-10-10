# 🦈 Lab 03 TCP Traffic Analysis with Wireshark.md

## Objective
Capture and analyze TCP network traffic using Wireshark to understand connection establishment, TCP flags, data transmission, connection termination, and retransmission behavior. Apply packet analysis techniques to investigate network activity from a SOC analyst perspective.


## Skills Demonstrated
TCP three-way handshake analysis

TCP flag identification (SYN, ACK, PSH, FIN, RST)

TCP source and destination port analysis

TCP stream reconstruction

TCP sequence and acknowledgment number interpretation

Connection termination analysis

TCP retransmission identification

Wireshark display filtering

Network connection investigation

PCAP evidence collection and documentation

## Tools used
Wireshark

Ubuntu Linux

Bash

Python 3

curl

ss

## Steps performed
Created a controlled local TCP service.

Captured TCP traffic using Wireshark.

Identified the TCP three-way handshake.

Examined TCP flags, sequence numbers, and acknowledgment numbers.

Followed a TCP stream to reconstruct application communication.

Analyzed TCP connection termination.

Inspected TCP retransmission indicators.

Documented findings from a simulated SOC investigation.


## evidence (screenshots
1)Created simple http server using these commands:

mkdir -p ~/soc-lab03-web

cd ~/soc-lab03-web

echo "SOC Lab 03 - TCP Analysis" > index.html

python3 -m http.server 8000 --bind 127.0.0.1

<img width="777" height="287" alt="image" src="https://github.com/user-attachments/assets/d0b1c068-1f80-404b-aa1a-39cd9eccfe3c" />

Then used the -ss ltnp | grep ':8000' in a different terminal 2 to confirm the service is listening.

2)Opened wireshark and selected the loopback interface, then filterd for tcp port 8000 using the tcp.port == 8000 filter on wireshark and then went back to terminal 2 on ubuntu and ran curl --http1.1 -H 'Connection: close' http://127.0.0.1:8000/ command to request the page server by my python server.

<img width="885" height="342" alt="image" src="https://github.com/user-attachments/assets/0414442c-5744-47aa-9910-32e09e5bb242" />

With this I was able to determine the following information:

Source IP: 127.0.0.1

Destination IP: 127.0.0.1

Source port: 42766 found in the transmission control protocol section inside wireshark

Destination port: 8000 found inside the same plane

TCP protocol: [SYN] which can be viewed in the info section

Number of packets in the conversation: 12 packets, as viewed in the conversation section of wireshark.

3) Identifying the 3 way handshake, used the tcp.port == 8000 && tcp.flags.syn == 1 to filter inside wireshark for the TCP flags.

<img width="877" height="122" alt="image" src="https://github.com/user-attachments/assets/dd297084-ff56-4698-aff3-4b4e45257118" />

Then used the tcp.port == 8000 && tcp.flags.syn == 1 && tcp.flags.ack == 0 filter to see the SYN packets without the ACK.

<img width="877" height="85" alt="image" src="https://github.com/user-attachments/assets/2b0796a6-5ec4-444f-9366-0ccf422578b7" />

Then used the tcp.port == 8000 && tcp.flags.syn == 1 && tcp.flags.ack == 1 to filter for only the syn-ack packets.

<img width="862" height="87" alt="image" src="https://github.com/user-attachments/assets/dda8932b-a7a2-454e-a011-80ebe56f5f67" 


4) opened the TCP stream inside wireshark, and was able to idenitfy the following information:

<img width="725" height="357" alt="image" src="https://github.com/user-attachments/assets/73092000-bde1-4e7b-b1df-bcd7a6c59cff" />

HTTP method: Get

Requested path: /

Host header: 127.0.0.1:8000


Response status: 200 OK

Response body: SOC Lab 03 - TCP Analysis


## SOC relevance 
SOC analysts use TCP packet analysis to investigate suspicious network connections, identify scanning patterns, validate network alerts, troubleshoot failed connections, and examine communication between endpoints.

Understanding TCP behavior helps distinguish normal network communication from potentially suspicious activity and supports evidence-based incident investigations.
