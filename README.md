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

