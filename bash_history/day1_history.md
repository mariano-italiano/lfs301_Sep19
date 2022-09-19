cd /tmp
ls
ls -l
ls -la
ls -la > wyjscie
cat wyjscie 
ls -la >> wyjscie
cat wyjscie 
rm wyjscie 
touch test
ls -la tes
ls -la test 
pwd
mkdir /root/test
cd
ls -la
touch test/plik1
ls -la test/
rmdir test/
rm -rf test/
ls -la
ls -la >& wyjscie
cat wyjscie 
su - student
vi plik1
vi
vi plik1
cat plik1
ls -la plik1 
clera
cls
clear
cat plik1 
sed 's/foo/linux/g' plik1 
sed 's/foo/linux/gI' plik1 
sed 's?/bin/bash?/bin/sh/g' plik1 
sed 's|/bin/bash|/bin/sh/g' plik1 
sed 's?/bin/bash?/bin/sh?g' plik1 
sed 's/\b[0-9]\{3}\b/number/g' plik1 
sed 's/\b[0-9]\{3\}\b/number/g' plik1 
sed 's/\b[0-9]\{3\}\b/liczba {&}/g' plik1 
sed 's/\b[0-9]\{3\}\b/& jest liczba/g' plik1 
cat plik1 
cat plik1 | grep -i foo
cat plik1 | grep -i foo -n
cat plik1 | grep Foo -n
cat plik1 | grep -v Foo
cat plik1 | grep foo -e -v 456
cat plik1 | grep -e foo -e 456
cat plik1 | grep -e foo -e 456 
cat plik1 | grep -e foo -e 456 | grep -v 456
cat plik1 >> plik1 
vi plik1 
cat plik1 | grep Foo -A 3 -B 5
less /var/log/messages
cat /var/log/messages | grep packagekitd -A 3 -B 1
less /var/log/messages
(END)
less /var/log/messages
grep 
grep root plik1 
grep Foo plik1 
grep Foo plik1 -n 
grep ^123 plik1 -n 
grep ^23 plik1 -n 
grep :/home/.*: /etc/passwd
man grep
find / -name plik1
find / -name plik1 -exec chown student:student {} \;
ls -la plik1 
ls -la
find /home -type d 
find /home -type d -maxdepth 2
find /home -type d -maxdepth 1
find /home/* -type d -maxdepth 1
find /h
man find
history
history > history-day1.md
find /home/* -type d -exec reboot \;
find /home/student/test -type d -exec reboot \;
man find
cd /tmp
ls -la
find . -name test -t d
find . -name test -type d
find . -name test -type f
cd
ping 192.168.190.6
vi /etc/hosts
ping almalinux
ssh-keygen --help
ssh-keygen -t rsa
ssh-copy-id root@almalinux
ssh 'root@almalinux'
ip a s
ssh 'root@almalinux'
cat .ssh/id_rsa
pssh
yum install pssh
yum repolist
yum clean all
yum repolist
yum install pssh
vi /etc/yum.repos.d/CentOS-Linux-AppStream.repo 
yum install pssh
vi /etc/yum.repos.d/CentOS-Linux-AppStream.repo 
yum install pssh
vi /etc/yum.repos.d/CentOS-Linux-BaseOS.repo 
ping wp.pl
ssh 'root@almalinux'
scp plik1 root@almalinux:/tmp/
ssh 'root@almalinux'
scp root@almalinux:/tmp/plikAlma . 
ls -la
ssh 'root@almalinux'
ps -ef
ps aux
ps --help
ps --help simple
ps --help list
man ps
ps -ef | grep sshd
ps -ef | grep sshd | grep -v grep
ps -ef | head
ps -ef | head -30
ps -ef | head -70
ps -ef 
pstree 
pstree -aAp
pstree -aAp sshd
pstree -aA sshd
pstree -a sshd
pstree -a ssh
ps -U student
man ps
ps -u student
ps -u student | wc -l
ps -U student | wc -l
ps -u student | wc -l
ps -U student | wc -l
ps -u student 
ps -C "bash"
ps -C "ssh"
ps -C "sshd"
pgrep sshd
pgrep -u student -l
pgrep -v -u student -l
ps aux -o pid,command
ps -o pid,command
ps aux -o pid,command
ps aux -o pid,cmd
ps -o pid,cmd
ps -e -o pid,cmd
ps -o pid,cmd
ps -e -o pid,uid,priority,cmd
unlimit --help
ulimit --help
vi skrypt.sh
chmod +x skrypt.sh
vi skrypt.sh
./skrypt.sh 
./skrypt.sh &
ps -ef | grep -i 3848
ps -e -o pid,uid,priority,cmd | grep 3848
ps -e -o pid,uid,priority,cmd 
ps -e -o pid,uid,priority,cmd | grep 3848
./skrypt.sh &
ps -e -o pid,uid,priority,cmd | grep 3882
ps -ef | grep -i 3848
ps -ef | grep -i 3882
nice -n 10 ./skrypt.sh &
ps -ef | grep -i 3914
ps aux | grep -i 3914
ps -e -o pid,cmd | grep -i 3914
ps -e -o pid,priority,cmd | grep -i 3914
renice -20 3914
ps -e -o pid,cmd | grep -i 3914
ps -e -o pid,cmd 
ps -e -o pid,priority,cmd | grep -i sshd 
ps -e -o pid,priority,cmd 
ulimit -n 1600
find / -name ulimits.conf
find / -name limits.conf
vi /etc/security/limits.conf
kill -l
ps -ef | grep -i ssh
kill -9 4177
kill -9 4190
ps -ef | grep -i ssh
kill -15 4409
kill -l
ps -ef | grep -i ssh
kill -19 4535
kill -18 4535
du -sh *
cd /var/log
du -sh *
du -sh * | grep -M
du -sh * | grep M
du -sh * | grep G
cd /
du -sh *
cd /ustr
cd /usr
du -sh *
df -h
cd
dnf repolist
vi /etc/yum.repos.d/google-chrome.repo 
dnf clean all
dnf repolist
vi /etc/yum.repos.d/CentOS-Linux-AppStream.repo 
dnf repolist
dnf install telnet
dnf update
sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
dnf update
dnf install pssh
dnf upgrade libmodulemd
dnf update
clear
cd /proc
ls -F
ls -F 4655
cat 4655/mem
ps -ef | grep 4655
cat 4655/cmdline 
ls -F tty/
ps -ef | grep ssh
ls -F 1784/
ls -F 1784/cmdline 
ls -F 1784/mem 
cat 1784/cmdline 
cat 1784/mem 
ls -la 1784/cmdline
ls -la 1784/mem
ls -la 1784/limits 
cat 1784/limits
cat 1784/stat
cat 1784/status
cat 1784/cwd
cat 1784/
clear
uname -r
uname -a
cd
wget http://mirror.centos.org/centos/7/os/x86_64/Packages/finger-0.17-52.el7.x86_64.rpm
dnf update
ls -la
rpm --help
rpm -ivh finger-0.17-52.el7.x86_64.rpm 
finger studen
finger student
rpm -qa
rpm -qa | sort > rpms.txt
less rpms.txt
rpm -e finger 
rpm -qa | grep finger
finger student
rpm -Va
rpm -qf /usr/bin/finger
rpm -ivh finger-0.17-52.el7.x86_64.rpm 
rpm -qf /usr/bin/finger
rpm -qi finger
cd /var/lib/rpm
ls -la
rpm --rebuilddb 
cd
rpm -qa | grep -i nano
dnf remove nano
rpm -qa | grep -i nano
dnf search nano
dnf install nano.x86_64
dnf provides "*/nano"
dnf install nano
rpm -qa | grep -i finger
rpm -e finger
dnf localinstall finger-0.17-52.el7.x86_64.rpm 
dnf grouplist
dnf group install "Security Tools"
dnf history list
dnf history undo 64
finger student
nano
dnf repolist
vi /etc/yum.repos.d/CentOS-Linux-AppStream.repo
cd /var/cache/dnf/
du -sh *
cd ..
du -sh * | grep -i dnf
dnf clean all
du -sh * | grep -i dnf
cd
dnf provides "*nano"
cd /etc/yum.repos.d/
ls -la
vi CentOS-Linux-HighAvailability.repo
echo http://vault.centos.org/$contentdir/$releasever/HighAvailability/$basearch/os/
cd
ls -la
mkdir /root/myRepo
cd /root/myRepo
mv /root/finger-0.17-52.el7.x86_64.rpm .
wget https://vault.centos.org/centos/8/BaseOS/x86_64/os/Packages/alsa-sof-firmware-1.8-1.el8.noarch.rpm
wget https://vault.centos.org/centos/8/BaseOS/x86_64/os/Packages/bind-export-libs-9.11.26-6.el8.i686.rpm
wget https://vault.centos.org/centos/8/BaseOS/x86_64/os/Packages/fxload-2008_10_13-10.el8.x86_64.rpm
ls -la
dnf install createrepo
wget https://vault.centos.org/centos/8/AppStream/aarch64/os/Packages/createrepo_c-0.17.2-3.el8.aarch64.rpm
ls -la
createrepo /root/myRepo
ls -la
cd repodata/
ls -la
less repomd.xml
cd ..
pwd
vi /etc/yum.repos.d/myRepo.repo
yum repolist
dnf install dnf-utils
dnf --help
dnf config-manager --help
dnf config-manager --enable file:///root/myRepo
mv /etc/yum.repos.d/myRepo.repo /etc/yum.repos.d/myRepo.tmp
dnf config-manager --enable file:///root/myRepo
dnf config-manager --enablerepo file:///root/myRepo
dnf config-manager --enablerepo file:///root/myRepo/
dnf config-manager --enablerepo /root/myRepo/
dnf config-manager --add-repo file:///root/myRepo/
vi /etc/yum.repos.d/
cd /etc/yum.repos.d/
ls
vi root_myRepo_.repo
dnf repolist
vi root_myRepo_.repo
dnf repolist
dnf config-manager --enablerepo myRepo
dnf config-manager --enablerepo file:///root/myRepo/
dnf config-manager --enablerepo root_myRepo
dnf config-manager --enablerepo root_myRepo_
dnf config-manager --enable root_myRepo_
dnf repolist
dnf module list
dnf module install nodejs
dnf module list
dnf module install php:7.4/devel
dnf module list
dnf module remove php
dnf module install php:7.3/devel
dnf module reset php
dnf module install php:7.3/devel
cd;clear
ip a
nmap 192.168.190.45/24
nmap 192.168.190.45/32
netstat --help
netstat -vatnulp
ip - link
ip -s link
netstat -vatnulp
ss -tunal
which netstat
dnf provides /usr/bin/netstat
ethtool -S ens160
iostat
uptime
cat /proc/cpuinfo 
cat /proc/cpuinfo | grep -i processor
netstat
netstat --help
netstat -i ens160
netstat -i 
vmstat 5
free -
free -m
sar -A
sar -B 3 3
sar -b 5 3
sar -q
sar --help
top
ls -la
nice 10 ./skrypt.sh &
nice -n 10 ./skrypt.sh &
top
ps -ef | grep 85694
ps aux | grep -i 85694
ps -efld | grep -i 85694
ps -efld 
top -u student
free -m
cat /proc/meminfo 
vmstat
cd /var/log/
ls -la
ls -la audit/
less audit/
less audit/audit.log 
less messages
cat messages | grep -i sshd
cat messages | grep -i ssh
less audit/audit.log 
less messages
less secure
less boot.log
dmesg -w
dmesg 
dnf install tuned
systemctl start tuned
tuned-adm list
tuned-adm active
tuned-adm profile balanced
tuned-adm active
tuned-adm recommend 
tuned-adm off
tuned-adm active
ls
cd
clear
dnf install git
git config --global user.name "Marcin"
git config --global user.email "markuj5@gmail.com"
git config --global -l
git config --global credential.helper store
git config --global -l
git clone https://github.com/mariano-italiano/lfs301_Sep19.git
ls
cd lfs301_Sep19 
ls -la
vi .git/config 
ls
git branch
mkdir bash_history
cd bash_history
history
history | awk '$1 > 780' | cut -c 8- > day1_history.md
