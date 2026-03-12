# Cyber-security
**changing file permissions:**
                                                                                                                                                                                                                                          
┌──(root㉿nitheesh)-[/home/nitheesh]
└─# ls -a
.     .bash_logout      .cache    data       .dmrc      eee         fund           .java   .localxpose  ni.html.save  .profile   sh.html                    Templates  Videos            .xsession-errors.old  .zsh_history
..    .bashrc           CamPhish  datamites  Documents  .face       .gnupg         kkk     .mozilla     nithee        Public     .ssh                       theni      .Xauthority       zphisher              .zshrc
ball  .bashrc.original  .config   Desktop    Downloads  .face.icon  .ICEauthority  .local  Music        Pictures      .recon-ng  .sudo_as_admin_successful  top        .xsession-errors  .zprofile
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh]
└─# cd fund  
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# pwd
/home/nitheesh/fund
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# touch fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# ls   
fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# ls -1
fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# ls -l
total 0
-rw-r--r-- 1 root root 0 Mar 10 02:09 fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# chmod 700 fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# ls -l
total 0
-rwx------ 1 root root 0 Mar 10 02:09 fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# chmod 755 fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# ls -l
total 0
-rwxr-xr-x 1 root root 0 Mar 10 02:09 fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# chmod 753 fine.txt
                                                                                                                                                                                                                                           
┌──(root㉿nitheesh)-[/home/nitheesh/fund]
└─# ls -l
total 0
-rwxr-x-wx 1 root root 0 Mar 10 02:09 fine.txt

**how to find subdomains:**

recon-ng][default] > db insert domains
domain (TEXT): h4cker.org
notes (TEXT): 
[*] 1 rows affected.
[recon-ng][default] > show domains

  +-------------------------------------------+
  | rowid |   domain   | notes |    module    |
  +-------------------------------------------+
  | 1     | h4cker.org |       | user_defined |
  +-------------------------------------------+

[*] 1 rows returned
[recon-ng][default] > modules load recon/domains-hosts/hackertarget
[recon-ng][default][hackertarget] > options set source h4cker.org
SOURCE => h4cker.org
[recon-ng][default][hackertarget] > run

----------
H4CKER.ORG
----------
[*] Country: None
[*] Host: backdoor.h4cker.org
[*] Ip_Address: 185.199.110.153
[*] Latitude: None
[*] Longitude: None
[*] Notes: None
[*] Region: None
[*] --------------------------------------------------
[*] Country: None
[*] Host: bootcamp.h4cker.org
[*] Ip_Address: 185.199.110.153
[*] Latitude: None
[*] Longitude: None
[*] Notes: None
[*] Region: None
[*] --------------------------------------------------
[*] Country: None
[*] Host: certs.h4cker.org
[*] Ip_Address: 198.185.159.145
[*] Latitude: None
[*] Longitude: None
[*] Notes: None
[*] Region: None

**what dns record type found?**

─$ dnsenum h4cker.org
dnsenum VERSION:1.3.1

-----   h4cker.org   -----


Host's addresses:
__________________

h4cker.org.                              5        IN    A        185.199.111.153
h4cker.org.                              5        IN    A        185.199.108.153
h4cker.org.                              5        IN    A        185.199.110.153
h4cker.org.                              5        IN    A        185.199.109.153


Name Servers:
______________

ns-cloud-c1.googledomains.com.           5        IN    A        216.239.32.108
ns-cloud-c2.googledomains.com.           5        IN    A        216.239.34.108
ns-cloud-c3.googledomains.com.           5        IN    A        216.239.36.108
ns-cloud-c4.googledomains.com.           5        IN    A        216.239.38.108

                                                                                                                                                                                                                                            
Mail (MX) Servers:                                                                                                                                                                                                                          
___________________                                                                                                                                                                                                                         
                                                                                                                                                                                                                                            
mxa.mailgun.org.                         5        IN    A        34.160.63.108                                                                                                                                                              
mxb.mailgun.org.                         5        IN    A        34.160.157.95

                                                                                                                                                                                                                                            
Trying Zone Transfers and getting Bind Versions:                                                                                                                                                                                            
_________________________________________________                                                                                                                                                                                           
                                                                                                                                                                                                                                            
                                                                                                                                                                                                                                            
Trying Zone Transfer for h4cker.org on ns-cloud-c2.googledomains.com ... 
AXFR record query failed: REFUSED

Trying Zone Transfer for h4cker.org on ns-cloud-c1.googledomains.com ... 
AXFR record query failed: REFUSED

Trying Zone Transfer for h4cker.org on ns-cloud-c4.googledomains.com ... 
AXFR record query failed: REFUSED

Trying Zone Transfer for h4cker.org on ns-cloud-c3.googledomains.com ... 
AXFR record query failed: REFUSED

                                                                                                                                                                                                                                            
Brute forcing with /usr/share/dnsenum/dns.txt:                                                                                                                                                                                              
_______________________________________________                                                                                                                                                                                             
                                                                                                                                                                                                                                            
lab.h4cker.org.                          5        IN    CNAME    santosomar.github.io.                                                                                                                                                      
santosomar.github.io.                    5        IN    A        185.199.111.153
santosomar.github.io.                    5        IN    A        185.199.109.153
santosomar.github.io.                    5        IN    A        185.199.108.153
santosomar.github.io.                    5        IN    A        185.199.110.153
mail.h4cker.org.                         5        IN    CNAME    pentestplus.github.io.
pentestplus.github.io.                   5        IN    A        185.199.111.153
pentestplus.github.io.                   5        IN    A        185.199.108.153
pentestplus.github.io.                   5        IN    A        185.199.109.153
pentestplus.github.io.                   5        IN    A        185.199.110.153
portal.h4cker.org.                       5        IN    CNAME    pentestplus.github.io.

**how many email address are discovered?**
using harvester
Target: h4cker.org 

Read api-keys.yaml from /etc/theHarvester/api-keys.yaml
        Searching 0 results.
[*] Searching Bing. 

[*] No IPs found.

[*] No emails found.

[*] No people found.

[*] No hosts found.

**What email domain pattern does the company use?**
dmitry -e h4cker.org  
Deepmagic Information Gathering Tool
"There be some deep magic going on"

HostIP:185.199.111.153
HostName:h4cker.org

**Gathered E-Mail information for h4cker.org***
---------------------------------
Searching Google.com:80...
Searching Altavista.com:80...
Found 0 E-Mail(s) for host h4cker.org, Searched 0 pages containing 0 results

All scans completed, exiting

**How many devices are active?**
**nmap -sn h4cker.org**
Starting Nmap 7.95 ( https://nmap.org ) at 2026-03-12 02:19 EDT
Nmap scan report for h4cker.org (185.199.111.153)
Host is up (0.0094s latency).
Other addresses for h4cker.org (not scanned): 185.199.109.153 185.199.110.153 185.199.108.153 64:ff9b::b9c7:6d99 64:ff9b::b9c7:6c99 64:ff9b::b9c7:6e99 64:ff9b::b9c7:6f99
rDNS record for 185.199.111.153: cdn-185-199-111-153.github.com
Nmap done: 1 IP address (1 host up) scanned in 0.46 seconds

**to find the gateway IP?**
**ip route**           
default via 192.168.254.2 dev eth0 proto dhcp src 192.168.254.128 metric 100 
192.168.254.0/24 dev eth0 proto kernel scope link src 192.168.254.128 metric 100 

**what is mail servers mx record?**
Mail (MX) Servers:                                                          mxa.mailgun.org.                         5        IN    A        34.160.13.42                                                                                                                                                              
mxb.mailgun.org.                         5        IN    A        34.149.236.64

**to find the IP address of the domain?**
nslookup h4cker.org
Server:         192.168.254.2
Address:        192.168.254.2#53

Non-authoritative answer:
Name:   h4cker.org
Address: 185.199.109.153
Name:   h4cker.org
Address: 185.199.111.153
Name:   h4cker.org
Address: 185.199.108.153
Name:   h4cker.org
Address: 185.199.110.153
Name:   h4cker.org
Address: 64:ff9b::b9c7:6c99
Name:   h4cker.org
Address: 64:ff9b::b9c7:6d99
Name:   h4cker.org
Address: 64:ff9b::b9c7:6f99
Name:   h4cker.org
Address: 64:ff9b::b9c7:6e99
**
**1.Who is the domain registrar? 2. When was the domain created? 3. Which organization owns it?**
**whois** h4cker.org tool
 whois h4cker.org
Domain Name: h4cker.org
Registry Domain ID: REDACTED
Registrar WHOIS Server: whois.squarespace.domains
Registrar URL: https://domains.squarespace.com
Updated Date: 2025-07-17T23:34:55Z
Creation Date: 2018-05-04T03:43:52Z
Registry Expiry Date: 2028-05-04T03:43:52Z
Registrar: Squarespace Domains II LLC
Registrar IANA ID: 895
Registrar Abuse Contact Email: abuse-complaints@squarespace.com
Registrar Abuse Contact Phone: +1.6466935324
Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
Name Server: ns-cloud-c1.googledomains.com
Name Server: ns-cloud-c2.googledomains.com
Name Server: ns-cloud-c3.googledomains.com
Name Server: ns-cloud-c4.googledomains.com
DNSSEC: signedDelegation
URL of the ICANN Whois Inaccuracy Complaint Form: https://icann.org/wicf/
>>> Last update of WHOIS database: 2026-03-12T06:29:44Z <<<

**Is a WAF present?
Which firewall vendor is used?**
**wafw00f** h4cker.org

                ______
               /      \                                                                                                                                                                                                                    
              (  W00f! )                                                                                                                                                                                                                   
               \  ____/                                                                                                                                                                                                                    
               ,,    __            404 Hack Not Found                                                                                                                                                                                      
           |`-.__   / /                      __     __                                                                                                                                                                                     
           /"  _/  /_/                       \ \   / /                                                                                                                                                                                     
          *===*    /                          \ \_/ /  405 Not Allowed                                                                                                                                                                     
         /     )__//                           \   /                                                                                                                                                                                       
    /|  /     /---`                        403 Forbidden                                                                                                                                                                                   
    \\/`   \ |                                 / _ \                                                                                                                                                                                       
    `\    /_\\_              502 Bad Gateway  / / \ \  500 Internal Error                                                                                                                                                                  
      `_____``-`                             /_/   \_\\                                                                                                                                                                                    
                                                                                                                                                                                                                                           
                        ~ WAFW00F : v2.3.1 ~                                                                                                                                                                                               
        The Web Application Firewall Fingerprinting Toolkit                                                                                                                                                                                
                                                                                                                                                                                                                                           
[*] Checking https://h4cker.org
[+] The site https://h4cker.org is behind Fastly (Fastly CDN) WAF.
[~] Number of requests: 2

****What usernames were found in metadata?
Which documents leaked internal information?
What country hosts the server?
What ISP owns IP?******
whois 185.199.109.153

% This is the RIPE Database query service.
% The objects are in RPSL format.
%
% The RIPE Database is subject to Terms and Conditions.
% See https://docs.db.ripe.net/terms-conditions.html

% Note: this output has been filtered.
%       To receive output for a database update, use the "-B" flag.

% Information related to '185.199.108.0 - 185.199.111.255'

% Abuse contact for '185.199.108.0 - 185.199.111.255' is 'abuse@github.com'

inetnum:        185.199.108.0 - 185.199.111.255
netname:        US-GITHUB-20170413
country:        US
org:            ORG-GI58-RIPE
admin-c:        GA9828-RIPE
tech-c:         NO1444-RIPE
status:         ALLOCATED-ASSIGNED PA
mnt-by:         RIPE-NCC-HM-MNT
mnt-by:         us-github-1-mnt
created:        2017-04-13T15:36:35Z
last-modified:  2025-01-21T15:14:18Z
source:         RIPE

organisation:   ORG-GI58-RIPE
org-name:       GitHub, Inc.
country:        US
org-type:       LIR
address:        88 Colin P. Kelly Jr. Street
address:        94107
address:        San Francisco
address:        UNITED STATES
phone:          +1 415 735 4488
admin-c:        GA9828-RIPE
tech-c:         NO1444-RIPE
abuse-c:        AR39914-RIPE
mnt-ref:        us-github-1-mnt
mnt-by:         RIPE-NCC-HM-MNT
mnt-by:         us-github-1-mnt
created:        2017-04-11T08:28:46Z
last-modified:  2020-12-16T13:16:10Z
source:         RIPE # Filtered

role:           GitHub Admin
address:        88 Colin P. Kelly Jr. Street
address:        94107
address:        San Francisco
address:        UNITED STATES
nic-hdl:        GA9828-RIPE
mnt-by:         us-github-1-mnt
created:        2017-04-18T22:16:30Z
last-modified:  2017-04-18T22:18:03Z
source:         RIPE # Filtered
abuse-mailbox:  abuse@github.com
org:            ORG-GI58-RIPE


geoiplookup 185.199.111.153
GeoIP Country Edition: US, United States
                                        


                                                                 

