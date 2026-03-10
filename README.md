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
