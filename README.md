# Cyber-security
changing file permissions:
                                                                                                                                                                                                                                          
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

how to find subdomains:
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

what dns record type found?
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

