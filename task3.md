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
## It's Complicated My Pal
* first by analayzing the pcap file using wireshark i could see lots of tcp and tls protocols
* Then i thought there might be some private key to decrypyt the TLS protocol
* I used find packet option in edit and searched for key but i couldn't find any
* Then i followed many tcp protocol and filtered http protoco but i couldn't find anything intresting
* Then by looking protocol hierarchy i could find icmp protocol 
* And i am not familiar with that protocol so searched on google and learnt basic things
* Then i could see flag.png inside a zip in the data of the packet
* So i tried to extract it using wireshark export bytes but there are more than 100 packets
* Then i tried to read the file in scapy but i couldnt read that its showing some errors
* Then i am in a situation to do nothing so i just used in binwalk and got a zip with password protected
* Tried to crack using john and fcrack but i couldnt
* Then i searched on google how to export data from pcap file other than wireshark and scapy
* Then i found a person having similiar problem he just solved it using tshark but it was too complicted to understand
* Then i saw a person below it providing simple tshark commands to extract
* Then i made slight changes on it and i could extract the zip and cracked using john
* Got the flag ```shellmates{icmp_p@y04d_4in't_us3l3ss_4ft3r_4ll_r1gHt?}```
##Dnscap
* working on it last stage :}
## Biz44re
* This was simple task for dedicated people there are more than 100 packets
* After analysing 3 to 4 times only i could find the starting point of this task
* There are lots of other protocols and i followed many tcp packtets and filtered dns and http
* But i could not find anything after solving its complicated my pal and i see few icmp protocol packets
* There is some hexadecimal value in three packets having icmp protocol
* Then i wrote a python script using scapy to export that and decoding i could see that its zip containing a png
* unzipped it got the flag ```inctf{_someTim3s_u_h4v3_to_l00k_3v3ryWh3r3_cl0s3r_TO_G3T_th3_wh0l3!}```
## Orcish
* This challenge can be easly solved by those who solved Bizaare easly
* It was also a similiar kind of challenge after solving bizaare and its complicated my pal
* I started focusing on icmp protocol.filtered those protocol and while looking the data
* Excecpt few all the packets have same data 
* Those fews has an additional letter as compared to that packets
* And this packets have error(unknown icmp(obsolete or malformed) in type field)
* while analysing 7 packets packets having this errors in the middle and by joining alphabet i could see the word lol nice
* Then wrote a python script using scapy for this to extract all the alphabet from type field having this error
* i could see a gif file but extracted the data but i couldnt open it :[
