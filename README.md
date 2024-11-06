### Date: 04/09/2024
# Ex-3: Google hacking and enumeration 

## AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

## Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:</br>

### Site: 
This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.</br>
Following searches for all the sites that is in the domain yahoo.com

#### Output:
![WhatsApp Image 2024-11-06 at 22 41 26_664df1c9](https://github.com/user-attachments/assets/3b32c072-e571-4945-ba49-f914f43f403a)



### filetype: 
This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com

#### Output:
![WhatsApp Image 2024-11-06 at 22 40 27_70b88171](https://github.com/user-attachments/assets/dae87367-a0a8-45b2-b1f3-feec50f5cbd5)


### Intext: 
This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.

#### Output:

![WhatsApp Image 2024-11-06 at 22 55 34_19b5c1c9](https://github.com/user-attachments/assets/57e80ef3-ffa3-43ba-97d6-d87150b8aaee)




### Inurl: 
This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.

#### Output:
![WhatsApp Image 2024-11-06 at 22 40 41_354cd628](https://github.com/user-attachments/assets/d6601d9e-cd88-4b18-877b-e59ef146bf05)




### Intitle: 
This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.

#### Output:

![5)](https://github.com/user-attachments/assets/3540cb17-cea2-4363-9f1d-720138f25eea)


### link: 
This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.

#### Output:

![6)](https://github.com/user-attachments/assets/aaaf006b-6c16-4fdd-909c-92cdeb721aee)




### Cache: 
This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.</br>

#### Output:

![7)](https://github.com/user-attachments/assets/0854f6c3-991a-4ea0-8013-1cb1e2d5ad80)

 
## DNS Enumeration


### DNS Recon
It provides the ability to perform:</br>
Check all NS records for zone transfers</br>
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration</br>
Top level domain expansion</br>
#### OUTPUT:



![8)](https://github.com/user-attachments/assets/abe37d80-5e64-406b-9b7f-2de94862c964)




### dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:</br>

Get the host’s addresses (A record).</br>
Get the namservers (threaded).</br>
Get the MX record (threaded).</br>
Perform axfr queries on nameservers and get BIND versions(threaded).</br>
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).</br>
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).</br>
Calculate C class domain network ranges and perform whois queries on them (threaded).</br>
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.</br>
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.</br>

#### Output:
![9)](https://github.com/user-attachments/assets/9a3d0c72-0893-4ac6-a2ca-89286c0b2c12)


### smtp-user-enum
Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.</br>


![10)](https://github.com/user-attachments/assets/570ccb52-8b35-4372-ba3b-c2dbbdc87e11)

In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:</br>

![11)](https://github.com/user-attachments/assets/e01f6b7a-d822-4e3c-a022-bc84c7816789)


select any username in the first column of the above file and check the same</br>


![12)](https://github.com/user-attachments/assets/98721fc1-33ed-476f-ae21-e3154e55ec2d)


## Telnet for smtp enumeration
Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect and issue appropriate commands.</br>
  
#### Output

![13)](https://github.com/user-attachments/assets/fa5bbc12-46a9-4cb9-b8c0-574a10243134)

  

### nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.</br>


#### OUTPUT:
![14)](https://github.com/user-attachments/assets/18f9a285-f9b9-40fe-b1ce-7a66594e5aba)


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully
