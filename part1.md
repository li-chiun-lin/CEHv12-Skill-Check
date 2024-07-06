# Part I

## Scenario

You have been hired as a part of the Red Team at CEHORG, an IT and ITES organization that deals with advanced research and development in the field of information security. It has offices all over the country connected in real-time by its network infrastructure.

Your organization is worried about rising cybersecurity incidents and has entrusted you with a comprehensive security audit of the complete infrastructure.

CEHORG’s internal network consists of several subnets housing various organizational units like any large organization. The front office is connected to a separate subnet that connects to the company’s public-facing computers. The company has installed multiple kiosks to help customers understand their products and services. The front office also has Wi-Fi connectivity to cater to the users who carry their smartphones and laptops.

The CEHORG’s internal network is made up of Militarized and Demilitarized zones. As a security precaution, and by design, all the internal resource zones are configured with different subnet IPs. The militarized zone houses the application servers that provide application frameworks for various departments. The Demilitarized Zone contains public-facing systems of the organization, such as web and mail servers. The headquarter’s network topology and protocols are replicated worldwide in all its satellite offices for easy communication with the headquarters.

### Challenge 1

You are performing reconnaissance for CEHORG and has been assigned a task to find out the physical location of one of their webservers hosting www.certifiedhacker.com. What are the GEO Coordinates of the webserver? Note: Provide answer as Latitude, Longitude. (Format: NN.NNN, *NN.NNN)

__hint:__ tools.keycdn.com

### Challenge 2

Identify if the website www.certifiedhacker.com allows DNS zone transfer. (Yes/No) (Format: Aa)

__hint:__ dig axfr www.certifiedhacker.com

### Challenge 3

Identify the number of live machines in 172.16.0.0/24 subnet. (Format: N)

__hint:__ sudo nmap -sn -PU 172.16.0.0/24

### Challenge 4

Find the IP address of the machine which has port 21 open. Note: Target network 172.16.0.0/24 (Format: NNN.NN.N.NN)

__hint:__ nmap -p 21 172.16.0.0/24

### Challenge 5

Find the IP address of the Domain Controller machine in 10.10.10.0/24. (Format: NN.NN.NN.NN)

__hint:__ nmap -p 53 172.16.0.0/24

### Challenge 6

Perform a host discovery scanning and identify the NetBIOS name of the host at 10.10.10.25. (Format: AAAAAAAAA)

__hint:__ nmap --script smb-os-discovery.nse 10.10.10.25

### Challenge 7

Perform an intense scan on 10.10.10.25 and find out the FQDN of the machine in the network. (Format: AaaaaAaaa.AAAAAA.aaa)

__hint:__ nmap --script smb-os-discovery.nse 10.10.10.25

### Challenge 8

What is the DNS Computer Name of the Domain Controller? (Format: AaaaaAaaa.AAAAAA.aaa)

__hint:__ nmap --script smb-os-discovery.nse 10.10.10.25

### Challenge 9

While performing a security assessment against the CEHORG network, you came to know that one machine in the network is running OpenSSH and is vulnerable. Identify the version of the OpenSSH running on the machine. Note: Target network 192.168.0.0/24. (Format: N.NaN)

__hint:__
1. nmap -p 22 192.168.0.0/24
2. nmap -sV 192.168.0.55

### Challenge 10

During a security assessment, it was found that a server was hosting a website that was susceptible to blind SQL injection attacks. Further investigation revealed that the underlying database management system of the site was MySQL. Determine the machine OS that hosted the database. (Format: Aaaaaa)

__hint:__ nmap -sV 192.168.0.55

### Challenge 11

Perform LDAP enumeration on the target network and find out how many user accounts are associated with the domain. (Format: N)

__hint:__ ldapsearch -h 10.10.10.25 -x -b "DC=CEHORG,DC=com" "objectclass=user" sAMAccountName sAMAccountType

### Challenge 12

Perform an LDAP Search on the Domain Controller machine and find out the version of the LDAP protocol. (Format: AAAAaN)

__hint:__ ldapsearch -h 10.10.10.25 -x -s base namingcontexts

### Challenge 13

What is the IP address of the machine that has NFS service enabled? Note: Target network 192.168.0.0/24. (Format: NNN.NNN.N.NN)

__hint:__ nmap 192.168.0.0/24

### Challenge 14

Perform a DNS enumeration on www.certifiedhacker.com and find out the name servers used by the domain. (Format: aaN.aaaaaaaa.aaa, aaN.aaaaaaaa.aaa)

__hint:__ dig ns www.certifiedhacker.com

### Challenge 15

Find the IP address of the machine running SMTP service on the 192.168.0.0/24 network. (Format: NNN.NNN.N.NN)

__hint:__ nmap 192.168.0.0/24

### Challenge 16

Perform an SMB Enumeration on 192.168.0.51 and check whether the Message signing feature is enabled or disabled. Give your response as Yes/No. (Format: Aaa)

__hint:__ nmap -p 445 -A 192.168.0.51

### Challenge 17

Perform a vulnerability research on CVE-2022-30171 and find out the base score and impact of the vulnerability. (Format: N.N Aaaaaa)

__hint:__ nvd.nist.gov/vuln/detail/cve-2022-30171

### Challenge 18

Perform vulnerability scanning for the domain controller using OpenVAS and identify the number of vulnerabilities with severity level as "medium". (Format: N)

__hint:__
1. sudo gvm-start
2. https://127.0.0.1:9392
3. scan 10.10.10.25

### Challenge 19

Perform vulnerability scanning for the webserver hosting movies.cehorg.com using OpenVAS and identify the severity level of RPC vulnerability. (Format: N)

__hint:__
1. sudo gvm-start
2. https://127.0.0.1:9392
3. scan 192.168.0.51

### Challenge 20

Perform vulnerability scanning for the Linux host in the 172.16.0.0/24 network using OpenVAS and find the number of vulnerabilities with severity level as medium. (Format: N)

__hint:__
1. sudo gvm-start
2. https://127.0.0.1:9392
3. scan 172.16.0.0/24
