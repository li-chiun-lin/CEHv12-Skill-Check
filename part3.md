# Part III

## Scenario

You have been hired as a part of the Red Team at CEHORG, an IT and ITES organization that deals with advanced research and development in the field of information security. It has offices all over the country connected in real-time by its network infrastructure.

Your organization is worried about rising cybersecurity incidents and has entrusted you with a comprehensive security audit of the complete infrastructure.

CEHORG’s internal network consists of several subnets housing various organizational units like any large organization. The front office is connected to a separate subnet that connects to the company’s public-facing computers. The company has installed multiple kiosks to help customers understand their products and services. The front office also has Wi-Fi connectivity to cater to the users who carry their smartphones and laptops.

The CEHORG’s internal network is made up of Militarized and Demilitarized zones. As a security precaution, and by design, all the internal resource zones are configured with different subnet IPs. The militarized zone houses the application servers that provide application frameworks for various departments. The Demilitarized Zone contains public-facing systems of the organization, such as web and mail servers. The headquarter’s network topology and protocols are replicated worldwide in all its satellite offices for easy communication with the headquarters.

### Challenge 1

CEHORG suspects of a possible session hijacking attack on a machine in its network. The organisation has retained the network traffic data for the session at C:\Users\Admin\Documents in the EH Workstation – 2 as sniffsession.pcap. You have been assigned a task to perform an analysis and find out the protocol that has been used for sniffing on its network. (Format: AAA)

__hint:__ wireshark

### Challenge 2

You have been assigned a task to perform a clickjacking test on www.certifiedhacker.com that the CEHORG members widely use. Find out whether the site is vulnerable to clickjacking. (Format: Aaa)

__hint:__ ClickjackPoc

### Challenge 3

Perform an HTTP-recon on www.certifiedhacker.com and find out the version of Nginx used by the web server. (Format: N.NN.N)

__hint:__ (Windows 11) httprecon

### Challenge 4

An FTP site is hosted on a machine in the CEHORG network. Crack the FTP credentials, obtain the “flag.txt” file and determine the content in the file. (Format: Aaaaaaa*AAA)

__hint:__ hydra

### Challenge 5

Perform Banner grabbing on the web application movies.cehorg.com and find out the ETag of the respective target machine. (Format: "NaNNNNNaaaNaaNN*N")

__hint:__

1. nc -vv movies.cehorg.com 80
2. GET / HTTP/1.0 (ENTER * 2)

### Challenge 6

Identify the Content Management System used by www.cehorg.com. (Format: AaaaAaaaa)

__hint:__ whatweb

### Challenge 7

Perform web application reconnaissance on movies.cehorg.com and find out the HTTP server used by the web application. (Format: Aaaaaaaaa-AAA/NN.N)

__hint:__ what web

### Challenge 8

Perform Web Crawling on the web application movies.cehorg.com and identify the number of live png files in images folder. (Format: N)

__hint:__ OWASP ZAP

### Challenge 9

Identify the load balancing service used by eccouncil.org. (Format: aaaaaaaaaa)

__hint:__ lbd

### Challenge 10

Perform a bruteforce attack on www.cehorg.com and find the password of user adam. (Format: aaaaaaNNNN)

__hint:__ Burp Suite

### Challenge 11

Perform parameter tampering on movies.cehorg.com and find out the user for id 1003. (Format: Aaaaa)

__hint:__ Burp Suite. Use Jason/welcome as login credentials

### Challenge 12

Perform a SQL Injection attack on movies.cehorg.com and find out the number of users available in the database. Use Jason/welcome as login credentials. (Format: N)

__hint:__

1. login use Jason/welcome
2. View Profile
3. Right Click > Inspect Element > Console
4. document.cookie
5. copy message
6. sqlmap -u "http://movies.cehorg.com/viewprofile.aspx?id=1" --cookie="[the copied message]" --dbs
7. sqlmap -u "http://movies.cehorg.com/viewprofile.aspx?id=1" --cookie="[the copied message]" -D moviescope --tables
8. sqlmap -u "http://movies.cehorg.com/viewprofile.aspx?id=1" --cookie="[the copied message]" -D moviescope -T User_Login --dump

### Challenge 13

__hint:__

### Challenge 14

__hint:__

### Challenge 15

__hint:__

### Challenge 16

__hint:__

### Challenge 17

__hint:__

### Challenge 18

__hint:__

### Challenge 19

__hint:__

### Challenge 20

__hint:__
