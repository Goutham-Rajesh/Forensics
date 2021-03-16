# Tasks
## Beginner Challs
### 1.dns.pcap
* First i viewed the pcap using wireshark
* From the name of the pcap file its clear that its related to dns.
* filtered packets based on dns protocol
* Then followed the packets through udp stream and got the flag
* ```picoCTF{w4lt3r_wh1t3_2d6d3c6c75aa3be7f42debed8ad16e3b}```
### 2.http.pcap
* Viewed the pcap file using wireshark
* when i checked the packets i can see many get request to a web page and
  asking for user authentication.
* then i filtered the packets based on http protocol
* since its a http protocol the username and password data will sent as plain text.
* so i checked the post request and followed the packet in tcp stream.
* From there i found the flag as password ``picoCTF{n0ts3cur3_894a6546}``
