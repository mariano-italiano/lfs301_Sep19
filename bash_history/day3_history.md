journalctl -b
clear
vi /boot/
cd /boot/
ls
uname -r
less grub2/grub.cfg
cd ..
du -sh *
 ls -lah boot/
cd
sysctl -a
sysctl -a |wc -l
cd /proc/sys/
ls -la
cd vm/
cat swappiness 
echo "40" > /proc/sys/vm/swappiness 
sysctl -a | grep -i swappiness
vi /etc/sysctl.conf 
sysctl -a | grep -i swappiness
sysctl -h
sysctl -p
sysctl -a | grep -i swappiness
sysctl -a | grep -i echo
sysctl -a | grep -i icmp
vi /etc/sysctl.conf 
sysctl -p
vi /etc/sysctl.conf 
sysctl -p
cd
lsmod | grep -i vmxnet
lsmod | grep -i dm_crypt
lsmod 
lsmod | sort
lsmod | sort | wc -l 
cd /lib/modules
ls
uname -r
cd 4.18.0-240.22.1.el8_3.x86_64
ls -la
find . -type f -name '*.ko*'
find . -type f -name '*.ko*'|grep -i crypt
find . -type f -name '*.ko*'|grep -i ethernet
cd
modprobe e1000
lsmod | grep e1000
modinfo e1000
modeprobe --jelp
modeprobe --help
modprobe --help
modprobe -r e1000
lsmod | grep e1000
clear
cat /etc/passwd
less /etc/login.defs 
ls -la /etc/shadow 
vi /etc/shadow
ls -la /etc/shadow
vi /etc/shadow
less /etc/shadow
chage -l student
cat /etc/shadow | grep -i student
id student
finger student
cat /etc/passwd| grep -i student
su - student
chage -l student
chage --help
chage -M 10 student
chage -l student
chage -M 5 student
chage -d 0 student
chage -l student
chage -m 0 -M 99999 -I -1 -E -1 student
chage -l student
chage -m 0 -M 99999 -I -1 -E -1 student
chage -l student
vi /etc/login.defs 
which useradd
which adduser
ls -la /usr/sbin/useradd
ls -la /usr/sbin/adduser
useradd jan
cat /etc/passwd
vi /etc/profile
vi /etc/profile.d/sh.local 
vi /etc/default/
vi /etc/default/useradd 
vi /etc/skel/
cd /etc/skel/
ls -la
vi READEME.PLEASE
useradd zosia
ls -la /home/zosia/
vi .bash_profile 
vi .bashrc 
useradd --help
useradd -u 1200 -G 1001 -d /tmp/testusercombo -s /bin/sh -c "Cos tam" testusercombo
passwd testusercombo
cat /etc/passwd
ls -la /tmp/testusercombo
su - testusercombo
cd
userdel -r testusercombo
passwd -l student
passwd -u student
dnf install hashcat
hashcat -h | grep sha512
hashcat -m 1800 -a 0 hash.txt
wget https://github.com/danielmiessler/SecLists/blob/master/Passwords/Leaked-Databases/rockyou-20.txt
vi /etc/yum.repos.d/CentOS-Linux-AppStream.repo 
clear
groupadd finanse
goupadd ksiegowosc
groupadd ksiegowosc
cat /etc/group
cat /etc/passwd
usermod -G finanse jan
usermod -G ksiegowosc zosia
cat /etc/group | tail 
id zosia
vi /etc/group
id zosia
groupmod -n recepcja ksiegowosc 
id zosia
groupmod -g 1010 recepcja
id zosia
id jan
id zosia
groupadd ksiegowosc
usermod -G ksiegowosc zosia
id zosia
usermod -aG recepcja,finanse zosia
id zosia
usermod --help
vi /etc/group
useradd testuser -G testgroup
id testuser
userdel testuser ; groupdel testgroup 
vi /etc/group
clear
visudo 
vi /etc/sudoers
vi /etc/sudoers.d/student 
vi /etc/sudoers.d/finanse
visudo
vi /etc/sudoers.d/finanse
visudo
vi /etc/sudoers.d/finanse
id zosia
su - zosia
passwd zosia
su - zosia
vi /etc/sudoers.d/finanse
su - zosia
vi /etc/sudoers.d/finanse
su - zosia
visudo
clear
ls -la 
mkdir permissions
cd permissions/
touch plik1 plik2
ls -la 
umask
chmod 760 plik1
ls -la
chmod u+rwg g+rw o-r plik2
chmod u+rwx g+rw o-r plik2
chmod u+rwx,g+rw,o-r plik2
ls -la 
chmod -x plik2
ls -la 
cd
ls -la /tmp
su - student
su - zosia
ls -la /usr/bin/passwd 
umask
cd permissions/
ls -al
chmod +t .
ls -la 
mkdir shared
chmod 2655 shared/
ls -la shared/
mkdir /tmp/finanse
cd /tmp
chmod 2755 finanse/
chgrp finanse finanse/
ls -la finanse/
chown zosia finanse/
ls -la finanse/
su - zosia
id jan
su - jan
chmod 2775 /tmp/finanse/
su - jan
chmod +t /tmp/finanse/
su - jan
su - zosia
su - jan
su - jan
getfacl /tmp/finanse/
setfacl -m u:jan:w /tmp/finanse/plik1
su - jan
getfacl /tmp/finanse/
getfacl /tmp/finanse/plik1
setfacl -m u:jan:w /tmp/finanse
su - jan
getfacl /tmp/finanse/
setfacl -m u:jan:rw /tmp/finanse
setfacl -m u:jan:rw /tmp/finanse/plik1
su - jan
getfacl /tmp/finanse/
getfacl /tmp/finanse/plik1
setfacl -m u:jan:rwx /tmp/finanse
su - jan
groups
id jan
id zosia
setfacl -x u:jan:rw /tmp/finanse/plik1
setfacl -x u:jan /tmp/finanse/plik1
su - jan
ls -la /tmp/finanse/
getfacl /tmp/finanse/
setfacl -x u:jan /tmp/finanse/
getfacl /tmp/finanse/
su - jan
chmod 3750 /tmp/finanse/
setfacl -m u:jan:rw /tmp/finanse/plik1
su - jan
ls -la /tmp/finanse/
chmod 3750 /tmp/finanse/ -R
su - jan
ls -la /tmp/finanse/
umask 0777 
touch umaskfile
ls -la umaskfile
umask 0022
chmod 3755 /tmp/finanse/plik1-backup 
ls -la /tmp/finanse/
history 
history | awk '$1 > 802' | cut -c 8- >> lfs301_Sep19/bash_history/day3_history.md
journalctl -b
clear
vi /boot/
cd /boot/
ls
uname -r
less grub2/grub.cfg
cd ..
du -sh *
 ls -lah boot/
cd
sysctl -a
sysctl -a |wc -l
cd /proc/sys/
ls -la
cd vm/
cat swappiness 
echo "40" > /proc/sys/vm/swappiness 
sysctl -a | grep -i swappiness
vi /etc/sysctl.conf 
sysctl -a | grep -i swappiness
sysctl -h
sysctl -p
sysctl -a | grep -i swappiness
sysctl -a | grep -i echo
sysctl -a | grep -i icmp
vi /etc/sysctl.conf 
sysctl -p
vi /etc/sysctl.conf 
sysctl -p
cd
lsmod | grep -i vmxnet
lsmod | grep -i dm_crypt
lsmod 
lsmod | sort
lsmod | sort | wc -l 
cd /lib/modules
ls
uname -r
cd 4.18.0-240.22.1.el8_3.x86_64
ls -la
find . -type f -name '*.ko*'
find . -type f -name '*.ko*'|grep -i crypt
find . -type f -name '*.ko*'|grep -i ethernet
cd
modprobe e1000
lsmod | grep e1000
modinfo e1000
modeprobe --jelp
modeprobe --help
modprobe --help
modprobe -r e1000
lsmod | grep e1000
clear
cat /etc/passwd
less /etc/login.defs 
ls -la /etc/shadow 
vi /etc/shadow
ls -la /etc/shadow
vi /etc/shadow
less /etc/shadow
chage -l student
cat /etc/shadow | grep -i student
id student
finger student
cat /etc/passwd| grep -i student
su - student
chage -l student
chage --help
chage -M 10 student
chage -l student
chage -M 5 student
chage -d 0 student
chage -l student
chage -m 0 -M 99999 -I -1 -E -1 student
chage -l student
chage -m 0 -M 99999 -I -1 -E -1 student
chage -l student
vi /etc/login.defs 
which useradd
which adduser
ls -la /usr/sbin/useradd
ls -la /usr/sbin/adduser
useradd jan
cat /etc/passwd
vi /etc/profile
vi /etc/profile.d/sh.local 
vi /etc/default/
vi /etc/default/useradd 
vi /etc/skel/
cd /etc/skel/
ls -la
vi READEME.PLEASE
useradd zosia
ls -la /home/zosia/
vi .bash_profile 
vi .bashrc 
useradd --help
useradd -u 1200 -G 1001 -d /tmp/testusercombo -s /bin/sh -c "Cos tam" testusercombo
passwd testusercombo
cat /etc/passwd
ls -la /tmp/testusercombo
su - testusercombo
cd
userdel -r testusercombo
passwd -l student
passwd -u student
dnf install hashcat
hashcat -h | grep sha512
hashcat -m 1800 -a 0 hash.txt
wget https://github.com/danielmiessler/SecLists/blob/master/Passwords/Leaked-Databases/rockyou-20.txt
vi /etc/yum.repos.d/CentOS-Linux-AppStream.repo 
clear
groupadd finanse
goupadd ksiegowosc
groupadd ksiegowosc
cat /etc/group
cat /etc/passwd
usermod -G finanse jan
usermod -G ksiegowosc zosia
cat /etc/group | tail 
id zosia
vi /etc/group
id zosia
groupmod -n recepcja ksiegowosc 
id zosia
groupmod -g 1010 recepcja
id zosia
id jan
id zosia
groupadd ksiegowosc
usermod -G ksiegowosc zosia
id zosia
usermod -aG recepcja,finanse zosia
id zosia
usermod --help
vi /etc/group
useradd testuser -G testgroup
id testuser
userdel testuser ; groupdel testgroup 
vi /etc/group
clear
visudo 
vi /etc/sudoers
vi /etc/sudoers.d/student 
vi /etc/sudoers.d/finanse
visudo
vi /etc/sudoers.d/finanse
visudo
vi /etc/sudoers.d/finanse
id zosia
su - zosia
passwd zosia
su - zosia
vi /etc/sudoers.d/finanse
su - zosia
vi /etc/sudoers.d/finanse
su - zosia
visudo
clear
ls -la 
mkdir permissions
cd permissions/
touch plik1 plik2
ls -la 
umask
chmod 760 plik1
ls -la
chmod u+rwg g+rw o-r plik2
chmod u+rwx g+rw o-r plik2
chmod u+rwx,g+rw,o-r plik2
ls -la 
chmod -x plik2
ls -la 
cd
ls -la /tmp
su - student
su - zosia
ls -la /usr/bin/passwd 
umask
cd permissions/
ls -al
chmod +t .
ls -la 
mkdir shared
chmod 2655 shared/
ls -la shared/
mkdir /tmp/finanse
cd /tmp
chmod 2755 finanse/
chgrp finanse finanse/
ls -la finanse/
chown zosia finanse/
ls -la finanse/
su - zosia
id jan
su - jan
chmod 2775 /tmp/finanse/
nmtui
nmtui-hostname 
vi /etc/resolv.conf 
clear
nslookup wp.pl
cat /etc/services | grep dns
cat /etc/services | grep dns -i
cat /etc/services | grep -i ssh
cat /etc/services | grep -i 112
cat /etc/services | grep -i ntp
cat /etc/services | grep -i nfs
cat /etc/services | grep -i rpc
cat /etc/resolv.conf 
nslookup vmware.com
nslookup 
clear
dig -t ns wp.pl
dig -t mx wp.pl
host wp.pl
cat /etc/hosts
vi /etc/nsswitch.conf
vi /etc/hosts
nslookup wp.pl
vi /etc/nsswitch.conf
nslookup wp.pl
ping wp.pl
vi /etc/nsswitch.conf
ping wp.pl
systemctl status firewalld.service 
firewall-cmd --reload
firewall-cmd --list-all
firewall-cmd --state
firewall-cmd --get-default-zone 
firewall-cmd --get-zones
firewall-cmd --set-default-zone=trusted
firewall-cmd --set-default-zone=trusted --permanent
firewall-cmd --list-all
firewall-cmd --reload
firewall-cmd --set-default-zone=public
firewall-cmd --reload
firewall-cmd --zone=public --list-ports
firewall-cmd --zone=public --add-port=2222/tcp --permanent
firewall-cmd --zone=public --add-service=https --permanent
firewall-cmd --reload
firewall-cmd --list-all
firewall-cmd --zone=public --list-services 
firewall-cmd --list-services 
firewall-cmd --get-services 
vi /etc/firewalld/services/
cd /etc/firewalld/services/
ls -la
ls -la /usr/lib/firewalld/services/
ls -la 
ls -la /usr/lib/firewalld/services/myservice.xml
firewall-cmd --new-service=myservice --permanent
ls -la /usr/lib/firewalld/services/myservice.xml
firewall-cmd --reload
ls -la /usr/lib/firewalld/services/myservice.xml
find / -name myservice.xml
vi /etc/firewalld/services/myservice.xml
firewall-cmd --permanent --service=myservice --set-description=Moj serwis sshd na 2222
firewall-cmd --permanent --service=myservice --set-description="Moj serwis sshd na 2222"
firewall-cmd --permanent --service=myservice --set-port=2222/tcp
firewall-cmd --permanent --service=myservice --add-port=2222/tcp
firewall-cmd --reload
vi /etc/firewalld/services/myservice.xml
vi /usr/lib/firewalld/services/ssh.xml 
vi /etc/firewalld/services/myservice.xml
vi /usr/lib/firewalld/services/ssh.xml 
vi /etc/firewalld/services/myservice.xml
firewall-cmd --zone=public --add-service=mysshd --permanent
systemctl restart firewalld.service 
firewall-cmd --zone=public --add-service=mysshd --permanent
firewall-cmd --zone=public --add-service=myservice --permanent
firewall-cmd --list-all
firewall-cmd --reload
firewall-cmd --list-all
firewall-cmd --new-zone webservers --permanent
firewall-cmd --reload
firewall-cmd --get-zones
firewall-cmd --change-interface=ens160 --zone webservers --permanent 
firewall-cmd --list-all
firewall-cmd --get-active-zones 
history
cd
history | awk '$1 > 802' | cut -c 8- >> lfs301_Sep19/bash_history/day3_history.md
